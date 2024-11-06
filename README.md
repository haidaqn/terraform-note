# Terraform

## Giới thiệu

Terraform là một công cụ mã nguồn mở được sử dụng để xây dựng, thay đổi và phiên bản hóa cơ sở hạ tầng một cách an toàn và hiệu quả. Terraform được phát triển bởi HashiCorp và hỗ trợ nhiều nhà cung cấp dịch vụ đám mây như AWS, Azure, Google Cloud, và nhiều hơn nữa.

## Tính năng chính

- **Hạ tầng như mã (Infrastructure as Code)**: Terraform cho phép bạn định nghĩa cơ sở hạ tầng của mình bằng mã, giúp dễ dàng quản lý và theo dõi các thay đổi.
- **Nhà cung cấp đa dạng**: Hỗ trợ nhiều nhà cung cấp dịch vụ đám mây và các dịch vụ khác nhau.
- **Quản lý trạng thái**: Terraform lưu trữ trạng thái của cơ sở hạ tầng để theo dõi các thay đổi và đảm bảo tính nhất quán.
- **Kế hoạch trước khi thực hiện**: Terraform cung cấp khả năng xem trước các thay đổi sẽ được thực hiện trước khi áp dụng chúng.

## Cài đặt

Để cài đặt Terraform, bạn có thể làm theo các bước sau:

1. Tải xuống phiên bản Terraform phù hợp với hệ điều hành của bạn từ trang chủ [Terraform](https://www.terraform.io/downloads.html).
2. Giải nén tệp tin đã tải xuống và thêm đường dẫn đến thư mục chứa tệp thực thi `terraform` vào biến môi trường `PATH`.

## Ví dụ cơ bản

Dưới đây là một ví dụ cơ bản về cách sử dụng Terraform để tạo một phiên bản EC2 trên AWS:

```hcl
provider "aws" {
    region = "us-west-2"
}

resource "aws_instance" "example" {
    ami           = "ami-0c55b159cbfafe1f0"
    instance_type = "t2.micro"

    tags = {
        Name = "example-instance"
    }
}
```

Để áp dụng cấu hình này, bạn có thể chạy các lệnh sau:

```sh
terraform init
terraform plan
terraform apply
```

## Tài liệu tham khảo

- [Tài liệu chính thức của Terraform](https://www.terraform.io/docs)
- [Hướng dẫn sử dụng Terraform](https://learn.hashicorp.com/terraform)

## Kết luận

Terraform là một công cụ mạnh mẽ giúp quản lý cơ sở hạ tầng một cách hiệu quả và an toàn. Bằng cách sử dụng Terraform, bạn có thể dễ dàng định nghĩa, triển khai và quản lý cơ sở hạ tầng của mình trên nhiều nhà cung cấp dịch vụ đám mây khác nhau.