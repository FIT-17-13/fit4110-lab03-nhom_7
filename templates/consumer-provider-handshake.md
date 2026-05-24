# Consumer–Provider Handshake

## Thông tin chung

- Lab: FIT4110 Lab 03
- Ngày: 2026-05-25
- Provider team: team-vision
- Consumer team: team-camera-analytics
- Provider service: AI Vision
- Consumer service: Camera Analytics

## Contract

- Contract file: contracts/ai-vision.openapi.yaml
- Mock base URL: http://localhost:4011
- Auth method: Bearer token
- Endpoint được test: POST /detect

## Smoke test

### Request

```http
POST /detect
Authorization: Bearer {{authToken}}
Content-Type: application/json
```

```json
{
	"camera_id": "CAM01",
	"image_url": "https://example.com/frame.jpg"
}
```

### Expected response

```json
{
	"detection_id": "DET001",
	"camera_id": "CAM01",
	"label": "person",
	"confidence": 0.91,
	"risk_level": "medium"
}
```

## Kết quả

- [x] Consumer gọi mock thành công.
- [x] Consumer parse được field cần dùng.
- [x] Consumer hiểu lỗi 4xx/5xx provider trả về.
- [x] Có Newman report hoặc screenshot.

## Ghi chú thay đổi hợp đồng

| Nội dung | Trước | Sau | Người đồng ý |
|---|---|---|---|
| | | | |

## Xác nhận

- Provider representative: Team Vision
- Consumer representative: Minh Quan
