# Độ khó là một thách thức: Thiết kế chế độ khó trong game

Trong bài viết chuyên sâu này, nhà thiết kế Boutros phân tích kỹ lưỡng về độ khó trong game, đặt câu hỏi: làm thế nào để các nhà sáng tạo có thể thêm vào những thử thách độc đáo, cấp cao, vừa gây hứng thú nhưng không làm nản lòng những người chơi có kỹ năng.

[Trong bài viết chuyên sâu này, vốn được đăng lần đầu trên tạp chí Game Developer, nhà thiết kế Boutros phân tích kỹ lưỡng về độ khó trong game, đặt câu hỏi: làm thế nào để các nhà sáng tạo có thể thêm vào những thử thách độc đáo, cấp cao, vừa gây hứng thú nhưng không làm nản lòng những người chơi có kỹ năng.]

Các chế độ độ khó trong game hiếm khi được bàn luận như một yếu tố quan trọng trong ngành. Ở một số game, chúng được bổ sung cẩn thận, phục vụ cho nhóm người chơi “hardcore”. Ở các game khác, chúng chỉ là ý nghĩ thêm vào sau, để làm hài lòng nhà phát hành, hoặc để cố gắng định hướng nhiều nhóm người chơi khác nhau bị thu hút bởi cùng một sản phẩm.

Đối với gần như mọi nhà phát triển, chế độ độ khó thường chỉ được xử lý vào cuối dự án, khi game đang được tinh chỉnh, và rất khó để thực hiện tốt nếu không đầu tư nhiều thời gian và suy nghĩ.

Trong bài viết này, tôi sẽ cố gắng khám phá một số phương pháp và triết lý đằng sau việc cách chơi khó đã được áp dụng thành công trong game, dù là về độ khó tổng thể, hay thông qua một mục tiêu tùy chọn mang tính tái định nghĩa cách chơi (như mục tiêu mở khóa đặc biệt siêu khó trong chế độ nhiều người chơi của GoldenEye trên Nintendo 64).

Chúng ta sẽ xem xét nơi nào một số phương pháp đã thành công, thất bại, và nơi nào chúng không còn phù hợp nữa. Vì độ khó là vấn đề mang tính chủ quan, tôi sẽ tập trung lập luận xung quanh các ý sau:

“Người chơi phải luôn cảm thấy rằng việc thất bại trong một thử thách hoàn toàn là trách nhiệm của bản thân, chứ không phải do sản phẩm được thiết kế kém.”

“Người chơi phải hiểu được cách và lý do tại sao mình thất bại, để họ có thể rút kinh nghiệm và tăng thêm cảm giác rằng thất bại là trách nhiệm của bản thân.”

Việc lựa chọn chế độ khó cao là hành động thể hiện mong muốn được thử thách của người chơi. Phần thưởng khi vượt qua thử thách là cảm giác giá trị và thành tựu—và để thử thách trở nên thú vị, nó cần vừa khó khăn vừa khả thi. Việc tinh chỉnh độ khó một cách nhanh chóng và hời hợt cũng có thể làm thay đổi căn bản cách chơi—điều này là thứ mà nhiều nhà phát triển chưa thực sự cân nhắc đủ trong quyết định của mình.


# Tinh chỉnh để tạo thử thách

Nhiều game đã cố gắng sao chép mô hình tăng độ khó của GoldenEye trên N64 của Rare—tăng gấp đôi sát thương từ kẻ địch = game khó hơn—nhưng trong bối cảnh các yếu tố khác, việc làm này thực chất có thể thay đổi kiểu chơi cốt lõi vốn nhất quán của game, từ đó làm thay đổi trải nghiệm theo một cách căn bản và có thể gây hụt hẫng.

Giả sử có một game FPS hư cấu tên là NaziShoot 2000. Ở chế độ thường, người chơi có thể bị bắn, có một giây để suy nghĩ, hồi phục rồi phản ứng. Nhưng ở chế độ khó, người chơi không thể mạo hiểm bị bắn, vì sát thương và AI tăng khiến họ gần như chết ngay lập tức.

Điều này buộc người chơi phải di chuyển và hành động thận trọng hơn. Trong một game khó được thiết kế lý tưởng, người chơi hoàn toàn có thể đi hết game mà không chết, nếu họ cực kỳ cẩn thận và tính toán. Tuy nhiên, game này phải kịp hạn chót, nên chế độ khó chỉ được phát triển từ chế độ thường rồi tinh chỉnh theo công thức. Trong tình huống nghẽn cổ chai kiểu “ghi nhớ” này, các pha bắn tỉa bất ngờ vào đầu và việc học từ thử–sai trở thành lối chơi chính.

Và đây là điểm khác biệt: trong khi chế độ thường thiên về phản xạ với chút ghi nhớ, thì chế độ khó lại trở thành trải nghiệm cổ điển dựa vào thử–sai, với việc ghi nhớ là kiểu chơi cốt lõi. Cách duy nhất để người chơi sống sót với ít tài nguyên và bất lợi về sát thương là thử, chết, ghi nhớ, rồi chơi lại.

Đây là nguyên tắc kinh điển của các game bắn súng 2D arcade đời cũ. Trong một game 3D, nơi trục bổ sung khiến người chơi phải lo nhiều hơn, độ phức tạp điều khiển tăng lên, và các chuỗi gameplay cốt lõi—như bắn kẻ địch rồi nhặt vật phẩm tăng lực—bị trải dài hơn do quy mô thế giới vật lý lớn hơn. Nếu người chơi có thể chết chỉ bằng một cú đánh, hoặc bởi các cơ chế chí mạng khác, điều này thường dẫn đến cảm giác ức chế dữ dội, và rất có thể khiến người chơi không hài lòng với game nói chung.


# Tổng hợp cách tinh chỉnh độ khó

Có nhiều yếu tố trong gameplay có thể tinh chỉnh để tạo chế độ khó hơn, miễn là có đủ thời gian để thử nghiệm kỹ với các chế độ khác và với người chơi ở nhiều trình độ khác nhau. Tôi sẽ phân tích một vài yếu tố dưới đây.

**Giới hạn thời gian (Time limit).** Đây là cách tinh chỉnh độ khó kinh điển cho game đua xe, và một số game đi cảnh—buộc người chơi phải hoàn thành màn hoặc thử thách trong khoảng thời gian X. Điều này thường ép người chơi phải tìm lộ trình tối ưu và nhìn nhận công cụ định hướng theo một cách khác.  
Nếu Prince of Persia: Sands of Time khai thác tính phi tuyến, có lẽ chúng ta đã thấy mục tiêu giới hạn thời gian được dùng để tái định nghĩa màn chơi theo nhiều cách thú vị. Thông thường, các game đua xe có cấu trúc thưởng theo huy chương, trong đó huy chương vàng đòi hỏi thời gian rất khắt khe. Các game có thêm yếu tố phụ trong đua xe—ví dụ F-Zero có chiến đấu—sẽ buộc người chơi tối ưu cả phần đó bên cạnh việc tìm đường lý tưởng.

**Cơ chế sát thương (Damage Dynamics).** Đây là yếu tố dễ nhất để chỉnh khi muốn làm game khó hơn—chỉ cần khiến mọi thứ gây nhiều sát thương hơn. Vấn đề là nếu không tinh chỉnh kỹ các yếu tố khác, như vị trí kẻ địch hay tài nguyên, thì dễ dẫn đến tình trạng “chết ngay lập tức”. Trong khoảng 5–10 phút chơi, điều này sẽ khiến game trở nên lười biếng và bất công. Đây cũng là cách dễ nhất để biến game từ dạng đánh giá/giải quyết sang dạng chơi dựa chủ yếu vào ghi nhớ.  
Những chế độ khó tốt nhất trong game thường chia sẻ một công thức chung: tăng độ khó dựa theo bối cảnh màn chơi. Đôi khi điều này là thêm lượt kẻ địch, thường thì là tăng sát thương, và đôi khi là giảm đạn dược.

**“Simon says”.** Với những game phụ thuộc vào nhấn nút, như DDR, Beatmania, hay Guitar Hero, việc yêu cầu nhiều lần nhấn hơn trong cùng một đơn vị thời gian là hợp lý để tăng độ khó. Áp lực tăng lên khi người chơi phải xử lý những gì họ thấy và kết hợp với những gì tay, chân hay ngón đang làm.

**AI hung hăng hơn (Increased AI aggression).** Halo 1 và 3 là ví dụ hoàn hảo, cũng như các bản Call of Duty do Infinity Ward phát triển. Đôi khi, kẻ địch đơn giản là hành động hung hăng hơn, buộc người chơi phản ứng nhanh và quyết đoán, thay vì chờ đợi để ngắm bắn hoàn hảo. Trong Halo, lính grunt sẽ lao vào tự sát ở chế độ khó.  
Hãy làm cho AI kẻ địch mạo hiểm hơn, nhưng đừng biến chúng thành những kẻ có thể nhìn thấy người chơi từ khoảng cách “triệu dặm” với độ chính xác của chim ưng gắn tia laser. Nếu không, bạn sẽ gặp tình huống kiểu Mega Man, nơi người chơi cảm thấy bị “ăn gian” bởi một cái chết bất ngờ ngoài tầm nhìn, chẳng hạn một viên đạn từ ngoài màn hình. Trong một số bối cảnh thì có thể thực tế, nhưng hầu hết những game kiểu này tôi từng chơi thì hiếm khi thú vị. Có thể chỉ là tôi, nhưng nó đã khiến tôi bỏ Medal of Honor: Airborne.

**Giảm vùng an toàn (Reduced neutral zones).** Đây là khi các khu vực an toàn hoặc khu vực không dùng đến bị loại bỏ hoặc thay thế bằng chướng ngại, ví dụ như gai nhọn không đứng được hoặc vùng chết ngay lập tức. Các màn Challenge trong Portal của Valve là ví dụ tuyệt vời. Điều này còn có tác dụng buộc người chơi tập trung vào rất ít lựa chọn, và nếu thiết kế màn tốt có thể tạo ra môi trường giải đố áp lực cao.

**Giới hạn HUD (HUD restrictions).** Trong một số game, độ khó có thể được tăng bằng cách thay đổi giao diện. Các game có nhiều hệ thống phản hồi hoạt động tốt nhất, vì việc tước đi hoặc hạn chế chỉ một “giác quan” trong game có thể khiến việc ra quyết định của người chơi trở nên căng thẳng hơn. Series Metal Gear Solid đã làm điều này từ đầu, khi độ khó cao sẽ loại bỏ radar trong game, buộc người chơi phải dựa vào trí nhớ về bản đồ, phản xạ, và hiểu biết về hành vi AI để sống sót.

**Hạn chế tài nguyên (Resource stinginess).** Series Resident Evil chọn cách giới hạn đạn khi độ khó tăng. Điều này tạo ra sự căng thẳng tột độ, vừa góp phần tăng yếu tố kinh dị, vừa tạo thêm áp lực buộc người chơi phải biết tận dụng. Nhiều cao thủ chế độ Professional trong Resident Evil 4 dựa vào kỹ năng bắn vào đầu gối để quật ngã kẻ địch, rồi kết liễu bằng dao nhằm vượt qua game với số đạn ít nhất.


# Ảo giác về sự công bằng

Một quan niệm phổ biến cho rằng chìa khóa để giữ cho thử thách vui vẻ với nhiều người chơi là làm cho nó *có vẻ* công bằng. Tất nhiên, những kịch bản game kinh điển—như một người chống lại cả đội quân quái vật ngoài hành tinh, hay một đĩa bay chống lại hàng loạt hạm đội tàu vũ trụ—thì hoàn toàn chẳng công bằng chút nào.

Ít có game nào, nếu có, là “công bằng” thực sự. Điều quan trọng là tạo *ảo giác công bằng* cho người chơi, và điều này được thực hiện thông qua các cơ chế tiện lợi. Bao gồm: hộp hồi máu đặt trước và sau những đoạn có nhiều kẻ địch, vật phẩm đạn dược được rải hào phóng, ma trận mạnh/yếu của vũ khí so với kẻ địch hiện diện trên màn hình, và hệ thống checkpoint hợp lý, thường được đặt trước và sau các khu vực khó. Quan trọng hơn cả là giao tiếp và phản hồi với người chơi. Sau đây là một vài ví dụ:

**Phản hồi vật lý.** Đây là tiêu chuẩn trong nhiều game FPS, nhưng Resistance: Fall of Man lại thiếu (sau đó game đã được vá để hỗ trợ tay cầm rung mới của Sony), và theo tôi, game đã bị ảnh hưởng nặng nề. Ngoài các yếu tố rõ ràng như vũ khí khai hỏa hay phương tiện di chuyển, hầu hết game ngày nay đều dùng phản hồi từ tay cầm để báo hiệu mức độ nguy hiểm nhân vật đang gặp phải.  
Ví dụ, nếu tay cầm chỉ rung nhẹ, người chơi đang bị tấn công nhưng chưa cận kề cái chết, hoặc bị bắn từ xa bằng đạn yếu. Nếu rung mạnh, khả năng cao là kẻ địch đang tấn công ở cự ly gần, hoặc bằng đòn gây sát thương lớn khiến nhân vật sắp chết.

**Phản hồi mối nguy.** Các dấu hiệu như viền màn hình đỏ nhấp nháy và hiệu ứng lọc màn hình rất hữu ích trong game 3D, nơi nhân vật có thể bị tấn công từ mọi hướng. Half-Life là game tiên phong với 4 vệt đỏ để báo hiệu sát thương đến từ phía nào—trước, sau, trái hay phải. Sau này, Call of Duty cải tiến bằng cách xác định chính xác góc bắn.

**Phản hồi thất bại.** Điều này khá hiếm trong game. Thông thường, tính năng này được coi là không cần nếu game được thiết kế chặt chẽ. Một số game, như Burnout (game đua xe nổi tiếng được giới phê bình khen ngợi), dùng tính năng phát lại ngay lập tức. Team Fortress 2 cũng làm rất tốt trong việc cho người chơi biết họ chết như thế nào. Khi bị hạ gục, kẻ địch hạ bạn sẽ được hiển thị ngay trên màn hình, phá vỡ ảo giác rằng thất bại là do game thiết kế tệ—ảo giác mà nhiều “tay thua cay cú” (bao gồm cả tôi) thường mắc phải.


# Lưu game và Checkpoint

Checkpoint có thể chia rẽ ý kiến người chơi, nhất là khi các điểm này được đặt cách xa nhau để tăng độ khó. Một số người cảm thấy rằng việc phải chơi qua nhiều màn liên tiếp trong một khoảng thời gian dài rồi cuối cùng mới thành công mới là “hardcore” thực sự. Ngược lại, nhiều người cho rằng lưu game và checkpoint nên được coi là một cơ chế tiện lợi và cần được cung cấp hào phóng, với triết lý “mỗi 5–10 phút” làm cốt lõi.

Thực tế, việc đặt checkpoint xa nhau thử thách sự kiên nhẫn và trí nhớ nhiều không kém gì kỹ năng, điều này có thể gây ức chế và khiến người chơi bỏ game. Call of Duty 2 có hệ thống checkpoint tốt nhất mà tôi từng trải nghiệm ở thế hệ mới, và Call of Duty 4 còn mở rộng hơn nữa. Không chỉ mỗi đoạn cao trào trong chế độ veteran đều có thể hoàn thành trong vòng 5–10 phút (đặc biệt trong Call of Duty 2), mà người chơi còn có checkpoint lưu được trước và sau cảnh cắt (cut-scene), tránh tình trạng lặp lại những khoảnh khắc nhàm chán như cảnh “Look at all dat juice” trong Gears of War.

Phần tai tiếng này của Gears of War buộc người chơi đối mặt với một nhóm kẻ địch Theron Guard cực mạnh đang tấn công một trạm bơm. Chết trong trận chiến đồng nghĩa với việc phải đi bộ lại một quãng dài trước khi trận đánh bắt đầu, và nghe lại đoạn thoại trong đó một nhân vật nói câu bất hủ “Look at all dat juice.” Việc lặp đi lặp lại điều này trở nên cực kỳ khó chịu.

Các nhiệm vụ phụ là lựa chọn thiết kế phổ biến khi hướng đến người chơi “hardcore”, cũng như các màn đặc biệt hoặc vật phẩm ẩn trong môi trường. Những game hướng đến người chơi trẻ như Jak and Daxter, Ratchet & Clank, và Lego Star Wars thường thưởng cho người chơi bằng auto-save khi tìm thấy vật phẩm ẩn. Gears of War cũng làm điều này với hệ thống COG Tag.

Điều hay ở đây là người chơi vẫn được thưởng cho nhiệm vụ họ đã hoàn thành, nhưng nếu chết, họ không cần làm lại từ đầu—chỉ cần tập trung vào thử thách chính của gameplay.

Một số game, bao gồm nhiều FPS trên PC, dựa vào cơ chế “lưu mọi lúc mọi nơi” và cắt giảm checkpoint. Một số khác lại đặt checkpoint cách xa nhau, buộc người chơi phải làm lại tất cả nhiệm vụ nhỏ ở giữa, gây cực kỳ khó chịu cho những người thích hoàn thành mọi thứ (completists) và muốn thử thách kỹ năng thay vì thử thách kiên nhẫn. Black của EA Criterion là một trong những ví dụ mà tôi nhớ nhất về lỗi này.

Trong game đó, sau khi đi xuống đồi, bắn qua một cánh đồng, vào căn cứ, giết sạch và phá hủy mọi thứ, chỉ để rồi bị bắn chết khi đang rời đi, tôi phải chơi lại toàn bộ chuỗi này (20 phút chơi), và còn phải nhặt lại tất cả vật phẩm nhiệm vụ phụ, mất đúng từng ấy thời gian trong mỗi lần thử. Cuối cùng tôi cũng tìm ra lộ trình tối ưu và đạt mức kiên nhẫn “siêu phàm”, nhưng trước đó, tôi hoàn toàn ghét trải nghiệm này—chỉ vì một đoạn của một game vốn dĩ được thiết kế rất tốt.

Lý do phổ biến mà các nhà thiết kế đưa ra khi bị chỉ trích thường là: “người chơi không bắt buộc phải làm hết, đó là lỗi của họ vì chúng tôi đã làm nó tùy chọn.” Nhưng họ quên mất rằng chính những người chơi có xu hướng chọn chế độ khó hơn lại cũng là những người có xu hướng bắt buộc bản thân phải thu thập hết và hoàn thành mọi nhiệm vụ. Về bản chất, nhà thiết kế đang cố biện minh bằng ngôn từ, trong khi thực tế là họ quên mất sự thật về khán giả của mình. Đây là yếu tố then chốt để hiểu được toàn bộ ý nghĩa của các chế độ này.


# Số lượng kẻ địch

Điều này cũng có thể được hiểu là số lượng đạn trong các game bắn súng nhìn từ trên xuống, hoặc nói chung là bất kỳ sự gia tăng nào về mối nguy động học hoặc do AI điều khiển. Rõ ràng, càng nhiều yếu tố mà người chơi phải đối mặt, họ càng phải suy nghĩ nhanh hơn, áp lực và căng thẳng càng lớn, và vì thế cảm giác thỏa mãn khi thành công cũng cao hơn. Nhưng việc cân bằng giữa áp lực và khả năng hoàn thành thực sự là rất khó.

Ikaruga có lẽ đã làm điều này tốt. Đây là một game bắn súng 2D nhìn từ trên xuống với cơ chế đơn giản nhưng cũng khiến nó trở thành một phần game giải đố. Con tàu có hai mặt đen và trắng, có thể chuyển đổi bằng một nút bấm. Mặt trắng có thể hấp thụ đạn trắng và gây gấp đôi sát thương lên tàu đen. Mặt đen có thể hấp thụ đạn đen và gây gấp đôi sát thương lên tàu trắng.

Ở chế độ dễ, khi người chơi bắn một kẻ địch, nó chết và hết. Ở chế độ thường, kẻ địch bị giết bằng đạn cùng màu với tàu của người chơi sẽ phát nổ thành một loạt đạn. Ở chế độ khó, tất cả kẻ địch đều phát nổ thành loạt đạn. Ở mỗi cấp độ khó, yếu tố giải đố thay đổi một chút, buộc người chơi phải điều chỉnh kế hoạch hành động đã ghi nhớ và có thể phải phản xạ nhanh hơn. Điều này cũng góp phần tăng áp lực tổng thể.

Gradius, R-Type và các game bắn cuộn khác có yếu tố chơi dựa vào trí nhớ, khi người chơi cần biết hình dạng màn chơi và chuyển động, kết hợp với thử thách phản xạ ở tốc độ cao. Đây là cách điều chỉnh độ khó đơn giản nhất, như đã đề cập ở đầu bài. Việc thêm một tháp súng hay một kẻ địch trong FPS trên PC cũng có thể mang lại kết quả tương tự, đồng thời làm thay đổi “bản đồ trí nhớ” mà người chơi đã có về màn chơi.

Các game bắn cuộn thường rất phù hợp với cơ chế này, vì màn chơi nhỏ và các viên đạn có thể hoạt động tương đối “hữu cơ” trong một môi trường cố định, kết hợp lối chơi dựa vào trí nhớ với phản xạ, mặc dù người chơi thường chia sẻ các giải pháp tối ưu để vượt qua các game này.


# Độ phức tạp của thao tác điều khiển (Input Complexity)

Street Fighter là một trong những game đầu tiên tạo ra mối quan hệ “rủi ro – phần thưởng” giữa độ phức tạp của thao tác điều khiển và hành động trên màn hình. Trong một thời gian dài, chiêu “spinning piledriver” của Zangief được coi là “chén thánh” của sự phối hợp tay–mắt, đòi hỏi người chơi phải xoay tròn cần điều khiển một vòng đầy đủ rồi bấm đấm ở cự ly gần, phần thưởng là hút bay gần một phần ba thanh máu của đối thủ.

Rủi ro ở đây là phải tiếp cận thật gần đối thủ, kết hợp với việc xoay cần thật nhanh, nếu quá chậm hoặc không đúng khoảng cách thì Zangief sẽ nhảy lên và để lộ sơ hở. Trong khi đó, chiêu bắn cầu lửa của Ryu và Ken đơn giản hơn nhiều, chỉ cần xoay một phần tư vòng tròn rồi bấm đấm, có thể thực hiện ở bất kỳ khoảng cách nào.

Hệ quả của việc dùng độ phức tạp thao tác làm rào cản độ khó là nó đồng thời trở thành rào cản tiếp cận với người chơi mới, tức là tự động giới hạn số lượng khán giả, mặc dù về mặt văn hóa, nó đã định hình game trong suốt mười năm tiếp theo.

Điều thú vị là David Sirlin, trưởng nhóm thiết kế Super Street Fighter 2 Turbo HD Remix, đã quyết định thay đổi một số tổ hợp chiêu của bản gốc để dễ tiếp cận hơn—including cả chiêu spinning piledriver của Zangief. Sirlin tin rằng độ khó nên đến từ khía cạnh chiến lược và khả năng ứng biến, chứ không phải từ việc xoay tổ hợp nút.

“Tôi nghĩ [Super Street Fighter 2 Turbo HD Remix] tốt hơn nhiều với các lệnh dễ hơn,” Sirlin nói. “Thay vì T.Hawk và Fei Long gần như là những nhân vật ‘không thể chơi được’ [như trước đây], thì giờ họ khá dễ để bắt đầu và vui hơn nhiều.

Chiến thuật trong Street Fighter tốt hơn nhiều—chứ không tệ đi—khi cả hai người chơi đều có thể thi triển chiêu thức. Không phải việc giỏi game trở nên dễ dàng hơn chỉ vì các lệnh đặc biệt được nới lỏng. Mà đúng hơn là việc *có thể chơi được ngay từ đầu* trở nên dễ hơn.

Khi các cao thủ Mỹ chơi bản thử nghiệm, họ nói rằng nó còn thú vị về mặt chiến lược hơn trước. Các lệnh mới cho chiêu thức chỉ là một phần rất nhỏ trong đó. Quan trọng hơn cả là những thay đổi về cân bằng giúp các nhân vật vốn yếu trước đây có thể cạnh tranh công bằng hơn. Có nhiều cặp đấu trước đây rất nhàm chán vì một nhân vật có mẫu chiến thuật quá áp đảo để dựa vào. Giờ hầu hết những cái đó đã được giảm bớt, nhường chỗ cho những ‘mind-game’ mới thay thế các lối chơi máy móc cũ.

Người chơi Street Fighter mới, tôi hy vọng, sẽ khám phá một con đường thú vị hơn để cải thiện kỹ năng bằng cách tập trung vào các trận đấu chiến lược này, thay vì chỉ tập trung vào việc bấm đúng chiêu.”


# Huyền thoại về độ khó

Series Halo của Bungie thường được ca ngợi vì cách triển khai tuyệt vời chế độ chơi khó trong dạng “Legendary mode”. Không ngạc nhiên khi nhóm phát triển đã có một cách tiếp cận rất kỹ lưỡng để giới thiệu và tinh chỉnh lối chơi khó. Nhà thiết kế gameplay của Halo 3, Francois Boucher-Genesse, giải thích rằng không thể áp dụng một công thức chung cho tất cả.

“Không phải chúng tôi chỉ đơn giản tăng máu của mọi kẻ địch lên 200% rồi gọi đó là Legendary,” ông nói. “Mỗi nhiệm vụ đều có những điều chỉnh tùy chỉnh riêng. Theo nghĩa đó, chúng tôi khuyến khích người chơi đã có kinh nghiệm với Halo nên chơi ít nhất ở chế độ Heroic, vì như vậy họ mới thấy được toàn bộ quy mô của game.”

“Một công thức khá tương tự đã được dùng cho mọi game Halo,” Boucher-Genesse tiếp tục. “Điểm khác biệt là thời gian dành để tinh chỉnh và sửa lỗi, nhằm đảm bảo game vui ở mọi cấp độ khó. Tất cả các bản đều có nhiều kẻ địch hơn, mạnh hơn, chính xác hơn, và đạn bay nhanh hơn. Các tham số này được dùng với giá trị tương tự trong từng trường hợp.”

Khi công ty của bạn dành ngân sách cho việc tinh chỉnh các mức độ khó, kết quả là tuổi thọ của game được kéo dài và sự thích thú của người chơi ở mọi trình độ đều tăng. Hiển nhiên, game cần phù hợp với nhóm người chơi mục tiêu ở mọi cấp độ, cung cấp thử thách cho từng bộ kỹ năng. Một điều quan trọng cần nhớ, vốn ngày càng xuất hiện nhiều trong game gần đây, là người chơi thường không tự đánh giá đúng mức độ kỹ năng của bản thân. Họ có thể nghĩ mình giỏi hơn hoặc yếu hơn thực tế.

Trong Metal Gear Solid 3, người chơi được hỏi liệu họ đã từng chơi phiên bản trước của series chưa, và từ đó được gán một cấp độ khó phù hợp. Đây là một cách làm khá hợp lý, và Call of Duty 4 còn tiến xa hơn. Người chơi sẽ phải trải qua một khóa huấn luyện ở đầu game, khóa này đồng thời đo lường khả năng của họ và đưa ra gợi ý mức độ khó ở cuối.

Hầu hết người chơi sẽ chấp nhận gợi ý này khi nó đến trực tiếp từ trong bối cảnh của game, thay vì phải chọn từ một danh sách trước khi họ chạm tay vào gameplay. Khi tất cả yếu tố này được kết hợp, tuổi thọ của phần chơi đơn trong game được kéo dài đáng kể.

# Tham khảo:
- Dịch từ: https://www.gamedeveloper.com/design/difficulty-is-difficult-designing-for-hard-modes-in-games
