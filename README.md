# BussinessNetwork-AntiDDoS

1. Yêu cầu doanh nghiệp 
Doanh nghiệp bất động sản mong muốn xây dựng một hệ thống mạng và bảo 
mật toàn diện, nhưng vì không am hiểu sâu về công nghệ nên chúng tôi xin đề xuất 
một số yêu cầu cơ bản như sau: 
Mục tiêu chung:

        Chúng tôi cần một hệ thống mạng có thể kết nối tất cả các 
        phòng ban trong công ty và đảm bảo sự an toàn, đặc biệt là trước các cuộc tấn công 
        từ bên ngoài, như các cuộc tấn công mạng hay tấn công từ chối dịch vụ (DDoS). 
        Chúng tôi muốn hệ thống hoạt động liên tục, không bị gián đoạn ngay cả khi có sự 
        cố.
   
Yêu cầu về kết nối mạng: 

    Cần hệ thống mạng chia rõ ràng cho từng phòng ban 
    để đảm bảo thông tin giữa các phòng không bị lẫn lộn và có thể quản lý được ai đang 
    sử dụng mạng và ở đâu. Các phòng ban cụ thể gồm: -   

      Phòng Marketing - - - - 
      Phòng Chăm sóc khách hàng (CSKH) 
      Phòng Ban Giám đốc 
      Phòng Kế toán 
      Phòng IT và thiết bị  
Hệ thống cần đảm bảo tốc độ internet nhanh, không bị lag khi nhiều người truy 
cập cùng lúc. 
Dự phòng khi có sự cố: Nếu hệ thống mạng gặp trục trặc hoặc một đường 
truyền bị đứt, chúng tôi mong muốn vẫn có thể hoạt động bình thường qua một kết 
nối dự phòng khác.

Yêu cầu về bảo mật: 

      Doanh nghiệp rất lo lắng về các cuộc tấn công mạng, đặc 
      biệt là tấn công DDoS – khi hệ thống có thể bị quá tải bởi quá nhiều yêu cầu từ bên 
      ngoài. Chúng tôi cần một giải pháp bảo mật có thể chống lại điều này để tránh hệ 
      thống bị sập. 
      Cần một tường lửa mạnh mẽ để ngăn chặn các truy cập trái phép, bảo vệ các 
      dữ liệu quan trọng. 
Bảo vệ ứng dụng web: 

  
    Do có sử dụng các ứng dụng trên mạng, nên cần có giải 
    pháp bảo vệ các website, chống lại những cuộc tấn công vào các ứng dụng đó. 
Nếu có công cụ nào giúp ngăn chặn truy cập trái phép, hoặc giới hạn quyền 
truy cập khi có dấu hiệu bất thường, chúng tôi rất muốn triển khai. 
Yêu cầu về hệ thống server: 

    Chúng tôi cần một máy chủ Linux Server để quản 
    lý các dịch vụ nội bộ như quản lý tài khoản người dùng, chia sẻ tài liệu, và các dịch 
    vụ khác. 
2. Phân tích yêu cầu doanh nghiệp 
2.1 Mục tiêu chung
   

        Doanh nghiệp yêu cầu hệ thống mạng ổn định, bảo mật và có tính sẵn sàng 
        cao. Mục tiêu này nhấn mạnh vào việc hệ thống phải: - 
        Đảm bảo kết nối liên tục cho toàn bộ phòng ban. - - 
        Chống lại các cuộc tấn công mạng, đặc biệt là tấn công DDoS. 
        Không bị gián đoạn ngay cả khi một đường truyền hoặc phần cứng gặp 
        sự cố. 
2.2 Yêu cầu về kết nối mạng 


    Phân chia mạng cho các phòng ban: Doanh nghiệp muốn rõ ràng trong việc 
    chia hệ thống mạng cho từng phòng ban, điều này yêu cầu một hệ thống phân chia 
    VLAN (Virtual Local Area Network). Mỗi phòng ban sẽ có một VLAN riêng, đảm 
    bảo rằng các thiết bị từ mỗi phòng sẽ được cách ly với nhau về mặt mạng để tránh 
    xung đột và đảm bảo an ninh thông tin. 
    VLAN 10: Phòng Marketing  
    VLAN 20: Phòng CSKH 
    VLAN 30: Ban Giám đốc 
    VLAN 40: Phòng Kế toán, HR 
    VLAN 50: Phòng IT thiết bị 
Tốc độ internet và khả năng chịu tải: - 

    Do yêu cầu về tốc độ internet nhanh và khả năng hoạt động đồng thời 
    của nhiều người dùng, doanh nghiệp sẽ cần một hệ thống có băng thông 
    lớn, có khả năng mở rộng và chịu tải tốt. Điều này đòi hỏi một giải pháp 
    sử dụng: 
        - Switch Layer 3 để định tuyến lưu lượng mạng nội bộ giữa các VLAN, 
        tránh tắc nghẽn lưu lượng. 
       -  Switch SD-WAN và Firewall kép: Giải pháp sử dụng dual firewall kết 
        hợp với SD-WAN và 2 router cho phép tối ưu hóa đường truyền internet 
        và bảo mật. SD-WAN không chỉ giúp lựa chọn tuyến đường tốt nhất 
        dựa trên hiệu suất mà còn đảm bảo tính dự phòng khi xảy ra sự cố. Kết 
        hợp với 2 firewall chạy song song, hệ thống đảm bảo an toàn trước các 
        cuộc tấn công DDoS, giúp cải thiện tốc độ và bảo mật cho toàn bộ 
        doanh nghiệp. 
Khả năng dự phòng khi có sự cố: 

    Hệ thống cần tính sẵn sàng cao, đặc biệt là 
    trong trường hợp xảy ra sự cố với một trong các đường truyền mạng hoặc thiết bị. Sử 
    dụng 2 switch SD-WAN kết hợp với 2 switch Layer 3 giúp đảm bảo khả năng dự 
    phòng. Nếu một thiết bị gặp sự cố, thiết bị còn lại sẽ tự động chuyển sang làm việc 
    để tránh gián đoạn. 
2.3 Yêu cầu về bảo mật 
Chống DDoS: 

    Vấn đề lo ngại lớn nhất của doanh nghiệp là các cuộc tấn công DDoS, 
    điều này yêu cầu một hệ thống Anti-DDoS mạnh mẽ, được cấu hình 
    qua các firewall chuyên dụng: 
    
    - Cần 2 Firewall chống DDoS để ngăn chặn tấn công và lọc lưu lượng từ 
    bên ngoài. 
    - Tường lửa Fortigate có thể cung cấp các tính năng như Rate Limiting 
    (giới hạn tốc độ truy cập), Deep Packet Inspection (kiểm tra sâu gói 
    tin), và Application Layer Protection (bảo vệ lớp ứng dụng) để phát 
    hiện và ngăn chặn các cuộc tấn công từ sớm. 
Bảo vệ ứng dụng web: - 
    
    Vì doanh nghiệp có sử dụng các ứng dụng web, họ cần bảo vệ các ứng 
    dụng này khỏi các cuộc tấn công từ bên ngoài như SQL Injection, XSS. 
Do đó, cần triển khai: - - 

    Web Application Firewall (WAF) như ModSecurity để bảo vệ các ứng 
    dụng web khỏi các cuộc tấn công mạng từ lớp ứng dụng (Layer 7). 
    Mod_evasive giúp hạn chế truy cập không bình thường từ một địa chỉ 
    IP, ngăn chặn các cuộc tấn công DoS/DDoS lên các ứng dụng web. 
Bảo mật quyền truy cập:

    Để bảo vệ các tài nguyên quan trọng và ngăn chặn truy cập trái phép, 
    doanh nghiệp cần một cơ chế giới hạn quyền truy cập, cụ thể:
    Fail2Ban để phát hiện và chặn các địa chỉ IP có hành vi đăng nhập sai 
    nhiều lần, giúp ngăn ngừa tấn công brute-force. 
2.4 Yêu cầu về quản lý và giám sát 

Giám sát hệ thống: 
- Doanh nghiệp cần một cách dễ dàng quản lý và giám sát hệ thống để 
phát hiện sớm các sự cố và tấn công. Để đáp ứng nhu cầu này, cần triển 
khai: 
    
      Hệ thống quản lý tập trung cho các thiết bị mạng (switch, router, 
      firewall) thông qua một mạng quản lý riêng (Management Network). 
      Công cụ giám sát như NetFlow hoặc sFlow để theo dõi lưu lượng mạng, 
      phát hiện các dấu hiệu tấn công hoặc sự cố. 

Tự động cảnh báo: Các hệ thống giám sát cần có khả năng tự động gửi cảnh 
báo khi phát hiện có dấu hiệu bất thường hoặc có cuộc tấn công mạng đang diễn ra, 
giúp đội ngũ công nghệ có thể can thiệp kịp thời. 
2.5 Yêu cầu về hệ thống server 

    Doanh nghiệp cần một Linux Server để quản lý các dịch vụ nội bộ như: 
    Domain Controller: Quản lý các tài khoản người dùng, phân quyền truy 
    cập cho từng người. - 
    Dịch vụ DHCP, DNS: Đảm bảo việc cấp phát địa chỉ IP và phân giải 
    tên miền nội bộ. 
