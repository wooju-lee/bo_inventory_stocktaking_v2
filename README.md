# Inventory Stocktaking Prototype

IIC BO 재고 실사(Inventory Stocktaking) 프로토타입

## Demo

https://bo-inventory-stocktaking-v2.vercel.app/

## Features

- **실사 시작**: Brand / BP / Store / Location 선택 후 실사 생성
- **중복 방지**: 동일 Store + Location에 미확정(READY) 실사가 있으면 생성 불가
- **수량 입력**: 인라인 직접 입력 또는 엑셀 업로드
- **필수값 검증**: 실사 수량 전체 입력 + 차이 발생 시 조정 사유 필수
- **저장/승인 플로우**: Save → Confirm / Reject (Saved 상태에서도 수량 수정 가능)
- **실사 취소**: Confirm 전까지 취소 가능 (CANCELED)

## Status Model

| Work Status | Approve Status | 설명 |
|-------------|---------------|------|
| In Progress | READY | 실사 진행 중 |
| Saved | READY | 저장 완료, 승인 대기 |
| Saved | CONFIRMED | 승인 완료, 재고 반영 |
| Saved | REJECTED | 반려 |
| - | CANCELED | 취소 |

## Tech

- 단일 HTML 파일 (inline CSS/JS)
- Vercel 배포
