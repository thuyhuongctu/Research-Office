# Skill nghiên cứu cho trợ lý AI (không thuộc tác phẩm)

Mười lăm skill chép nguyên từ [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills),
commit `a1043ef544e3a100c28e70a736b6cf32554d0677` (12/10/2026). Giấy phép MIT,
toàn văn ở `LICENSE-K-Dense.md`; riêng `statsmodels` tự khai BSD-3-Clause trong
SKILL.md của nó. Không sửa ký tự nào.

Đây là **công cụ làm việc** cho Claude Code khi làm các bài thực nghiệm IB
(WBES, FDI), không phải một phần của văn phòng nghiên cứu: bị loại khỏi trang
Pages (`pages.yml` xoá thư mục này trước khi đóng gói) và khỏi bản lưu Zenodo
(`.gitattributes` đặt `export-ignore`).

| Nhóm | Skill |
| --- | --- |
| Định lượng | `statsmodels`, `statistical-analysis`, `statistical-power`, `exploratory-data-analysis`, `shap` |
| Tài liệu, trích dẫn | `literature-review`, `paper-lookup`, `citation-management`, `pyzotero` |
| Viết và phản biện | `scientific-writing`, `peer-review`, `scholar-evaluation`, `venue-templates` |
| Trình bày, tài trợ | `scientific-visualization`, `research-grants` |

Hai chỗ cần biết:

- `literature-review/scripts/generate_schematic_ai.py` gửi yêu cầu tới
  OpenRouter, nhưng **chỉ khi** có đặt `OPENROUTER_API_KEY`; không đặt thì
  không gửi gì.
- `research-grants` viết cho quỹ Mỹ và Đài Loan (NSF, NIH, NSTC); với NAFOSTED
  hay quỹ khác chỉ dùng được phần khung lập luận.

Cập nhật: chép lại thư mục `skills/<tên>` từ commit mới của kho gốc, rồi sửa
mã commit ở đầu tệp này.
