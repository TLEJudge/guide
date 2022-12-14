***[Tổng quan:]{.underline}***

***Đề thi bao gồm 11 bài, 14 trang (kể cả trang này), thời gian làm bài
225 phút (3 giờ 45 phút), bảng điểm được đóng băng sau 180 phút (3 giờ).
Contest tính theo luật của ICPC.***

***Giới hạn thời gian của ngôn ngữ Python bằng hai lần giới hạn thời
gian của các ngôn ngữ khác.***

  --------------------------------------------------------------------------------
              ***Tên bài***                  ***Giới hạn thời   ***Giới hạn bộ nhớ
                                             gian (s)***        (MB)***
  ----------- ------------------------------ ------------------ ------------------
  [*A*](#A)   *Chú mèo và những chiếc hộp    *5.0*              *256*
              (bản dễ)*                                         

  [*B*](#B)   *Chú mèo và những chiếc hộp    *5.0*              *256*
              (bản khó)*                                        

  [*C*](#C)   *Đường đi trên cây*            *1.0*              *512*

  [*D*](#D)   *Phần tử quan trọng*           *2.0*              *512*

  [*E*](#E)   *Đồng xu*                      *1.0*              *256*

  [*F*](#F)   *Chương trình*                 *2.0*              *256*

  [*G*](#G)   *SQRT + SQRT = SQRT? (bản dễ)* *3.0*              *256*

  [*H*](#H)   *SQRT + SQRT = SQRT? (bản      *3.0*              *256*
              vừa)*                                             

  [*I*](#I)   *SQRT + SQRT = SQRT? (bản      *3.0*              *256*
              khó)*                                             

  [*J*](#J)   *Dãy ngoặc*                    *5.0*              *512*

  [*K*](#K)   *Cây k-phân*                   *2.0*              *512*
  --------------------------------------------------------------------------------

***Cách "giao tiếp với máy chấm" (dành cho các bài interactive, ví dụ
như bài A):** Bạn phải flush output để máy chấm có thể đọc và ghi nhận
câu trả lời của bạn, bằng một số lệnh sau:*

-   *cout \<\< endl; hoặc cout \<\< flush; hoặc fflush(stdout); trong
    C++.*

-   *stdout.flush() trong Python.*

***Tất cả các bài đều có đúng 100 testcases.***

*\
*

[]{#A .anchor}***Bài A -- Chú mèo và những chiếc hộp (bản dễ)***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 5 giây*

*Giới hạn bộ nhớ: 256 MB*

***Đây là một bài tập giao tiếp với máy chấm. Bài A và B chỉ khác nhau ở
giới hạn của n.***

*Có một con mèo và n chiếc hộp được đánh số từ 1 đến n, ở ngày 0 con mèo
đang ở trong một hộp bất kỳ. Mỗi đêm, nó sẽ bò ra khỏi chiếc hộp của
mình và di chuyển sang chiếc hộp khác ở ngay cạnh chiếc hộp của nó, nói
cách khác, nếu con mèo đang ở hộp thứ i, nó sẽ đi sang chiếc hộp thứ*
$i - 1$ *(nếu* $i - 1 \geq 1$*) hoặc chiếc hộp thứ* $i + 1$ *(nếu*
$i + 1 \leq n$*). Mỗi buổi sáng, bạn sẽ đi đến những chiếc hộp và được
mở một chiếc hộp. Nếu bạn tìm thấy chú mèo, quá trình kết thúc. Nếu
không, bạn đóng chiếc hộp lại và để lại chỗ cũ.*

*Do sự kiên nhẫn của bạn có giới hạn, bạn chỉ có thể thực hiện quá trình
này trong không quá* $10^{5}$ *ngày.*

*Giới hạn: Với **bản dễ**,* $n \leq 10^{4}$*.*

*Giao tiếp với máy chấm:*

-   *Đầu tiên, chương trình của bạn cần phải nhập một số nguyên dương n
    là số chiếc hộp*

-   *Sau đó, quá trình sau sẽ lặp lại liên tục đến khi bạn trả lời chính
    xác hoặc vượt quá số truy vấn cho phép:*

```{=html}
<!-- -->
```
-   *Bạn đưa ra một số nguyên dương k (*$1 \leq k \leq n$*).*

-   *Nếu con mèo đang ở hộp thứ k, bạn sẽ nhập được một xâu có nội dung
    TRUE, chương trình của bạn kết thúc và bạn AC test đó, ngược lại,
    bạn sẽ nhập được một xâu có nội dung FALSE và bạn phải tiếp tục
    đoán.*

```{=html}
<!-- -->
```
-   *Nếu bạn vượt quá số truy vấn cho phép, bạn bị tính là sai test đó,
    đồng nghĩa với việc sai cả bài.*

*Ví dụ: (Lưu ý rằng ví dụ này không phản ánh chiến lược tối ưu)*

  ------------------------------------------------------------------------------------
  ***Input***   ***Output***   ***Giải thích***
  ------------- -------------- -------------------------------------------------------
  *5*                          *Máy chấm cho biết có 5 chiếc hộp. Con mèo hiện tại
                               đang ở hộp thứ 3.*

                *2*            *Bạn đoán con mèo đang ở hộp thứ 2.*

  *FALSE*                      *Bạn đoán không chính xác. Con mèo di chuyển sang hộp
                               2.*

                *3*            *Bạn đoán con mèo đang ở hộp thứ 3.*

  *FALSE*                      *Bạn đoán không chính xác. Con mèo di chuyển sang hộp
                               1.*

                *1*            *Bạn đoán con mèo đang ở hộp thứ 1.*

  *TRUE*                       *Bạn đoán chính xác, chương trình kết thúc và bạn được
                               tính điểm.*
  ------------------------------------------------------------------------------------

[]{#B .anchor}

***Bài B -- Chú mèo và những chiếc hộp (bản khó)***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 5 giây*

*Giới hạn bộ nhớ: 256 MB*

***Đây là một bài tập giao tiếp với máy chấm. Bài A và B chỉ khác nhau ở
giới hạn của n.***

*Có một con mèo và n chiếc hộp được đánh số từ 1 đến n, ở ngày 0 con mèo
đang ở trong một hộp bất kỳ. Mỗi đêm, nó sẽ bò ra khỏi chiếc hộp của
mình và di chuyển sang chiếc hộp khác ở ngay cạnh chiếc hộp của nó, nói
cách khác, nếu con mèo đang ở hộp thứ i, nó sẽ đi sang chiếc hộp thứ*
$i - 1$ *(nếu* $i - 1 \geq 1$*) hoặc chiếc hộp thứ* $i + 1$ *(nếu*
$i + 1 \leq n$*). Mỗi buổi sáng, bạn sẽ đi đến những chiếc hộp và được
mở một chiếc hộp. Nếu bạn tìm thấy chú mèo, quá trình kết thúc. Nếu
không, bạn đóng chiếc hộp lại và để lại chỗ cũ.*

*Do sự kiên nhẫn của bạn có giới hạn, bạn chỉ có thể thực hiện quá trình
này trong không quá* $10^{5}$ *ngày.*

*Giới hạn: Với **bản khó**,* $n \leq 5 \times 10^{4}$*.*

*Giao tiếp với máy chấm:*

-   *Đầu tiên, chương trình của bạn cần phải nhập một số nguyên dương n
    là số chiếc hộp*

-   *Sau đó, quá trình sau sẽ lặp lại liên tục đến khi bạn trả lời chính
    xác hoặc vượt quá số truy vấn cho phép:*

```{=html}
<!-- -->
```
-   *Bạn đưa ra một số nguyên dương k (*$1 \leq k \leq n$*).*

-   *Nếu con mèo đang ở hộp thứ k, bạn sẽ nhập được một xâu có nội dung
    TRUE, chương trình của bạn kết thúc và bạn AC test đó, ngược lại,
    bạn sẽ nhập được một xâu có nội dung FALSE và bạn phải tiếp tục
    đoán.*

```{=html}
<!-- -->
```
-   *Nếu bạn vượt quá số truy vấn cho phép, bạn bị tính là sai test đó,
    đồng nghĩa với việc sai cả bài.*

*Ví dụ: (Lưu ý rằng ví dụ này không phản ánh chiến lược tối ưu)*

  ------------------------------------------------------------------------------------
  ***Input***   ***Output***   ***Giải thích***
  ------------- -------------- -------------------------------------------------------
  *5*                          *Máy chấm cho biết có 5 chiếc hộp. Con mèo hiện tại
                               đang ở hộp thứ 3.*

                *2*            *Bạn đoán con mèo đang ở hộp thứ 2.*

  *FALSE*                      *Bạn đoán không chính xác. Con mèo di chuyển sang hộp
                               2.*

                *3*            *Bạn đoán con mèo đang ở hộp thứ 3.*

  *FALSE*                      *Bạn đoán không chính xác. Con mèo di chuyển sang hộp
                               1.*

                *1*            *Bạn đoán con mèo đang ở hộp thứ 1.*

  *TRUE*                       *Bạn đoán chính xác, chương trình kết thúc và bạn được
                               tính điểm.*
  ------------------------------------------------------------------------------------

[]{#C .anchor}

***Bài C -- Đường đi trên cây***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 1 giây*

*Giới hạn bộ nhớ: 512 MB*

*Cho n đỉnh và các thao tác nối các đỉnh lại với nhau bằng n - 1 cạnh có
trọng số, sao cho sau khi nối tất cả các cạnh sẽ tạo được một đồ thị
liên thông. Trong khi các thao tác nối đỉnh được thực hiện, người ta
muốn biết xem liệu có tồn tại đường đi giữa hai đỉnh của đồ thị hay
không, và trọng số của đường đi (nếu có) là bao nhiêu. Trọng số của một
đường đi giữa hai đỉnh trên cây được định nghĩa là tổng xor của trọng số
của tất cả các cạnh trên đường đi giữa hai đỉnh đó.*

*Input:*

-   *Dòng đầu tiên gồm hai số nguyên dương n, q lần lượt là số đỉnh và
    số truy vấn*

-   *q dòng tiếp theo, mỗi dòng có một trong hai định dạng sau:*

```{=html}
<!-- -->
```
-   *+ u v w: tạo một đường đi nối hai đỉnh u và v có trọng số w. Dữ
    liệu đầu vào đảm bảo có chính xác n -- 1 truy vấn loại này.*

-   *? u v: tính trọng số của đường đi giữa hai đỉnh u và v, nếu không
    có thì in ra -1.*

*Output:*

-   *Gồm nhiều dòng, mỗi dòng là kết quả của một truy vấn loại 2.*

*Giới hạn:* $n,\ q \leq 10^{6}$*.*

*Ví dụ*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *5*                               | *-1*                              |
|                                   |                                   |
| *? 1 5*                           | *2*                               |
|                                   |                                   |
| *+ 1 5 3*                         | *5*                               |
|                                   |                                   |
| *+ 5 3 1*                         | *7*                               |
|                                   |                                   |
| *? 1 3*                           | *-1*                              |
|                                   |                                   |
| *+ 5 2 6*                         | *2*                               |
|                                   |                                   |
| *? 2 1*                           | *5*                               |
|                                   |                                   |
| *? 2 3*                           |                                   |
|                                   |                                   |
| *? 2 4*                           |                                   |
|                                   |                                   |
| *+ 1 4 7*                         |                                   |
|                                   |                                   |
| *? 2 4*                           |                                   |
|                                   |                                   |
| *? 3 4*                           |                                   |
+-----------------------------------+-----------------------------------+

*Chú thích:*

-   *Truy vấn đầu tiên (hình 1): các đỉnh chưa được nối với nhau nên kết
    quả là -1.*

-   *Truy vấn thứ hai (hình 2): tồn tại đường đi 1 5 3 có trọng số là
    2.*

-   *Truy vấn thứ ba (hình 3): tồn tại đường đi 2 5 1 có trọng số là 5.*

-   *Truy vấn thứ tư (hình 3): tồn tại đường đi 2 5 3 có trọng số là 7.*

-   *Truy vấn thứ năm (hình 3): không tồn tại đường đi đến đỉnh 4.*

-   *Truy vấn thứ sáu (hình 4): tồn tại đường đi 2 5 1 4 có trọng số là
    2.*

-   *Truy vấn thứ bảy (hình 4): tồn tại đường đi 3 5 1 4 có trọng số là
    5.*

![C:\\Users\\DELL\\Downloads\\graph
(5).png](media/image1.png){width="2.8in"
height="2.8in"}![C:\\Users\\DELL\\Downloads\\graph
(6).png](media/image2.png){width="2.8in"
height="2.8in"}![C:\\Users\\DELL\\Downloads\\graph
(8).png](media/image3.png){width="2.8in"
height="2.8in"}![C:\\Users\\DELL\\Downloads\\graph
(7).png](media/image4.png){width="2.8in" height="2.8in"}

*\
*

[]{#D .anchor}***Bài D -- Phần tử quan trọng***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 2 giây*

*Giới hạn bộ nhớ: 512 MB*

*Cho một dãy số nguyên a gồm n phần tử và một số nguyên dương k. Một
phần tử* $a_{i}$ *được gọi là quan trọng khi và chỉ khi tồn tại một tập
các phần tử của dãy a (giá trị có thể trùng nhau nhưng vị trí bắt buộc
phải khác nhau) có chứa phần tử* $a_{i}$ *sao cho tổng các giá trị trong
tập này lớn hơn hoặc bằng k, nhưng khi bỏ đi số* $a_{i}$ *thì tổng các
số lại nhỏ hơn k. Hãy xác định xem mỗi phần tử trong dãy a có quan trọng
hay không.*

*Input:*

-   *Dòng đầu tiên là hai số nguyên dương.*

-   *Dòng tiếp theo chứa* $n$ *số nguyên dương của dãy a.*

*Output:*

-   *In ra một dãy nhị phân độ dài n, bit thứ i là 0 nếu phần tử thứ i
    không quan trọng và ngược lại.*

*Giới hạn:* $n,\ k \leq 10^{4},\ a_{i} \leq 10^{9}$*.*

*Ví dụ:*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *4 10*                            | *1010*                            |
|                                   |                                   |
| *4 1 6 2*                         |                                   |
+-----------------------------------+-----------------------------------+

*Giải thích:*

-   *Tồn tại tập {4; 6} có tổng lớn hơn hoặc bằng 10, nhưng khi bỏ một
    trong hai phần tử đó đi, tổng sẽ nhỏ hơn 10, vậy phần tử thứ 1 và
    thứ 3 là quan trọng.*

-   *Với các phần tử 1 và 2, để có được một tập có tổng lớn hơn hoặc
    bằng 10, tập đó phải có cả phần tử 4 và 6, nên khi bỏ phần tử 1 hoặc
    2 đi thì tổng vẫn không nhỏ hơn 10. Vậy phần tử thứ 2 và thứ 4 là
    không quan trọng.*

*\
*

[]{#E .anchor}***Bài E -- Đồng xu***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 1 giây*

*Giới hạn bộ nhớ: 256 MB*

*Cho một số nguyên dương n và k số nguyên dươnga*
$a_{1},a_{2},\ldots,a_{k} \leq 2n$*. Người ta bày sẵn 2n đồng xu trên
bàn sao cho có đúng n đồng xu ngửa và n đồng xu sấp. Với mỗi thao tác,
bạn có thể chọn một số bất kỳ trong tập a, giả sử số bạn chọn là t. Bạn
sẽ lấy các đồng xu liên tiếp (có thể không lấy đồng xu nào) có cùng
trạng thái (cùng sấp hoặc cùng ngửa), sau đó chuyển chúng ra đầu dãy. Ví
dụ:*

*Với trạng thái các đồng xu được đặt như sau: AAB[B]{.underline}BBAA (ký
hiệu A là mặt ngửa và B là mặt sấp) và t = 4, ta có thể thu được các
trạng thái sau:*

-   *[BBB]{.underline}AABAA (chuyển các đồng xu 3, 4, 5 lên đầu).*

-   *[BBBB]{.underline}AAAA (chuyển các đồng xu 3, 4, 5, 6 lên đầu).*

-   *\...*

*Hỏi rằng với dãy a đã cho, tồn tại hay không một cách sắp xếp các đồng
xu sao cho không thể có trường hợp n đồng xu đầu tiên có cùng một trạng
thái sau một số hữu hạn các thao tác?*

*Input:*

-   *Dòng đầu tiên gồm hai số nguyên dương* $n,\ k$*.*

-   *Dòng tiếp theo gồm các số nguyên dương miêu tả dãy a*.

*Output: In ra "YES" nếu tồn tại một cách sắp xếp các đồng xu sao cho
không thể khiến n đồng xu đầu tiên có cùng một trạng thái sau một số hữu
hạn các thao tác, và "NO" trong trường hợp ngược lại.*

*Giới hạn:* $n,\ a_{i} \leq 10^{9},\ k \leq 10^{6}$*.*

*Ví dụ:*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *4 4*                             | *NO*                              |
|                                   |                                   |
| *1 2 3 4*                         |                                   |
+-----------------------------------+-----------------------------------+
| *4 2*                             | *YES*                             |
|                                   |                                   |
| *1 2*                             |                                   |
+-----------------------------------+-----------------------------------+

*Giải thích: Ở trường hợp thứ 2 tồn tại cách sắp xếp ABABABAB.*

*\
*

[]{#F .anchor}***Bài F -- Chương trình***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 2 giây*

*Giới hạn bộ nhớ: 256 MB*

*Cho một hàm f được viết bằng ngôn ngữ C++ như sau (ở đây \^ là phép
xor, & là phép and, \<\< là phép dịch bit):*

long long f(long long a, long long b)

{

if(b == 0) return a;

else return f(a \^ b, (a & b) \<\< 1);

}

*Hỏi trong các số nguyên dương từ 1 đến n, có bao nhiêu cặp số (i, j)
(*$i \leq j$*) sao cho f(i, j) = i \^ j.*

*Input: Một dòng gồm duy nhất số nguyên dương n.*

*Output: số cặp số thoả mãn.*

*Giới hạn:* $n \leq 50000$*.*

*Ví dụ*

  -----------------------------------------------------------------------
  ***Input***                         ***Output***
  ----------------------------------- -----------------------------------
  *5*                                 *5*

  -----------------------------------------------------------------------

*Giải thich: Các cặp số thoả mãn là: (1, 2), (1, 4), (2, 4), (2, 5), (3,
4).*

*\
*

***Bài G -- SQRT + SQRT = SQRT? (bản dễ)***[]{#G .anchor}

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 3 giây*

*Giới hạn bộ nhớ: 256 MB*

***Các bài G, H, I chỉ khác nhau ở giới hạn của c.***

*Cho số nguyên không âm* $c$*, bạn cần đếm xem có bao nhiêu số nguyên
không âm* $a \leq c$ *sao cho* $\left( \sqrt{c} - \sqrt{a} \right)^{2}$
*là một số nguyên, hay nói cách khác là tồn tại số nguyên không âm b sao
cho* $\sqrt{a} + \sqrt{b} = \sqrt{c}$*.*

*Input:*

-   *Dòng đầu tiên gồm số nguyên dương* $T \leq 5$*, miêu tả số
    testcases.*

-   *T dòng tiếp theo mỗi dòng gồm 1 số nguyên không âm c.*

*Output: Gồm T dòng, mỗi dòng là số các số nguyên dương a thoả mãn điều
kiện, sắp xếp theo thứ tự không giảm.*

*Giới hạn: với **bản dễ**,* $c \leq 10^{6}$*.*

*Ví dụ*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *5*                               | *2*                               |
|                                   |                                   |
| *5*                               | *2*                               |
|                                   |                                   |
| *10*                              | *2*                               |
|                                   |                                   |
| *15*                              | *3*                               |
|                                   |                                   |
| *20*                              | *6*                               |
|                                   |                                   |
| *25*                              |                                   |
+-----------------------------------+-----------------------------------+

*Giải thích:*

-   $\sqrt{0} + \sqrt{5} = \sqrt{5}$*.*

-   $\sqrt{0} + \sqrt{10} = \sqrt{10}$*.*

-   $\sqrt{0} + \sqrt{15} = \sqrt{15}$*.*

-   $\sqrt{0} + \sqrt{20} = \sqrt{5} + \sqrt{5} = \sqrt{20}$*.*

-   $\sqrt{0} + \sqrt{25} = \sqrt{1} + \sqrt{16} = \sqrt{4} + \sqrt{9} = \sqrt{25}$*.*

*\
*

[]{#H .anchor}***Bài H -- SQRT + SQRT = SQRT? (bản vừa)***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 3 giây*

*Giới hạn bộ nhớ: 256 MB*

***Các bài G, H, I chỉ khác nhau ở giới hạn của c.***

*Cho số nguyên không âm* $c$*, bạn cần đếm xem có bao nhiêu số nguyên
không âm* $a \leq c$ *sao cho* $\left( \sqrt{c} - \sqrt{a} \right)^{2}$
*là một số nguyên, hay nói cách khác là tồn tại số nguyên không âm b sao
cho* $\sqrt{a} + \sqrt{b} = \sqrt{c}$*.*

*Input:*

-   *Dòng đầu tiên gồm số nguyên dương* $T \leq 5$*, miêu tả số
    testcases.*

-   *T dòng tiếp theo mỗi dòng gồm 1 số nguyên không âm c.*

*Output: Gồm T dòng, mỗi dòng là số các số nguyên dương a thoả mãn điều
kiện, sắp xếp theo thứ tự không giảm.*

*Giới hạn: với **bản vừa**,* $c \leq 10^{12}$*.*

*Ví dụ*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *5*                               | *2*                               |
|                                   |                                   |
| *5*                               | *2*                               |
|                                   |                                   |
| *10*                              | *2*                               |
|                                   |                                   |
| *15*                              | *3*                               |
|                                   |                                   |
| *20*                              | *6*                               |
|                                   |                                   |
| *25*                              |                                   |
+-----------------------------------+-----------------------------------+

*Giải thích:*

-   $\sqrt{0} + \sqrt{5} = \sqrt{5}$*.*

-   $\sqrt{0} + \sqrt{10} = \sqrt{10}$*.*

-   $\sqrt{0} + \sqrt{15} = \sqrt{15}$*.*

-   $\sqrt{0} + \sqrt{20} = \sqrt{5} + \sqrt{5} = \sqrt{20}$*.*

-   $\sqrt{0} + \sqrt{25} = \sqrt{1} + \sqrt{16} = \sqrt{4} + \sqrt{9} = \sqrt{25}$*.*

*\
*

[]{#I .anchor}***Bài I -- SQRT + SQRT = SQRT? (bản khó)***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 3 giây*

*Giới hạn bộ nhớ: 256 MB*

***Các bài G, H, I chỉ khác nhau ở giới hạn của c.***

*Cho số nguyên không âm* $c$*, bạn cần đếm xem có bao nhiêu số nguyên
không âm* $a \leq c$ *sao cho* $\left( \sqrt{c} - \sqrt{a} \right)^{2}$
*là một số nguyên, hay nói cách khác là tồn tại số nguyên không âm b sao
cho* $\sqrt{a} + \sqrt{b} = \sqrt{c}$*.*

*Input:*

-   *Dòng đầu tiên gồm số nguyên dương* $T \leq 5$*, miêu tả số
    testcases.*

-   *T dòng tiếp theo mỗi dòng gồm 1 số nguyên không âm c.*

*Output: Gồm T dòng, mỗi dòng là số các số nguyên dương a thoả mãn điều
kiện, sắp xếp theo thứ tự không giảm.*

*Giới hạn: với **bản khó**,* $c \leq 10^{18}$*.*

*Ví dụ*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *5*                               | *2*                               |
|                                   |                                   |
| *5*                               | *2*                               |
|                                   |                                   |
| *10*                              | *2*                               |
|                                   |                                   |
| *15*                              | *3*                               |
|                                   |                                   |
| *20*                              | *6*                               |
|                                   |                                   |
| *25*                              |                                   |
+-----------------------------------+-----------------------------------+

*Giải thích:*

-   $\sqrt{0} + \sqrt{5} = \sqrt{5}$*.*

-   $\sqrt{0} + \sqrt{10} = \sqrt{10}$*.*

-   $\sqrt{0} + \sqrt{15} = \sqrt{15}$*.*

-   $\sqrt{0} + \sqrt{20} = \sqrt{5} + \sqrt{5} = \sqrt{20}$*.*

-   $\sqrt{0} + \sqrt{25} = \sqrt{1} + \sqrt{16} = \sqrt{4} + \sqrt{9} = \sqrt{25}$*.*

*\
*

[]{#J .anchor}***Bài J -- Dãy ngoặc***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 5 giây*

*Giới hạn bộ nhớ: 512 MB*

*Một dãy ngoặc đúng được định nghĩa như sau:*

-   *() là một dãy ngoặc đúng.*

-   *Với A là một dãy ngoặc đúng, (A) cũng là một dãy ngoặc đugns.*

-   *Với A, B là các dãy ngoặc đúng, AB là một dãy ngoặc đúng.*

*Bạn được cho n dãy ngoặc. Nhiệm vụ của bạn là sắp xếp các dãy ngoặc này
thành một dãy ngoặc đúng.*

*Input:*

-   *Dòng đầu tiên gồm số nguyên dương n.*

-   *n dòng tiếp theo, mỗi dòng là một dãy ngoặc. Các dãy ngoặc được
    đánh số từ 1 đến n theo thứ tự xuất hiện ở input.*

*Output:*

-   *Nếu không tìm được hoán vị nào, in ra -1.*

-   *Nếu có, in ra n dòng gồm n số là hoán vị của dãy (1, 2, ..., n),
    mang ý nghĩa rằng nếu nối các dãy ngoặc theo thứ tự trong output sẽ
    cho ra một dãy ngoặc đúng. Nếu có nhiều cách nối, in ra một cách bất
    kỳ.*

*Giới hạn:*

-   $n \leq 10^{6}$*.*

-   *Tổng số lượng ký tự (không kể số n) không vượt quá* $10^{7}$*.*

*Ví dụ:*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *2*                               | *2*                               |
|                                   |                                   |
| *())())()*                        | *1*                               |
|                                   |                                   |
| *((()*                            |                                   |
+-----------------------------------+-----------------------------------+
| *5*                               | *1*                               |
|                                   |                                   |
| *(*                               | *5*                               |
|                                   |                                   |
| *))*                              | *2*                               |
|                                   |                                   |
| *((*                              | *3*                               |
|                                   |                                   |
| *))*                              | *4*                               |
|                                   |                                   |
| *(*                               |                                   |
+-----------------------------------+-----------------------------------+
| *2*                               | *-1*                              |
|                                   |                                   |
| *((*                              |                                   |
|                                   |                                   |
| *)*                               |                                   |
+-----------------------------------+-----------------------------------+

*\
*

[]{#K .anchor}***Bài K -- Cây k-phân***

*Input: Stardard input*

*Output: Stardard output*

*Giới hạn thời gian: 2 giây*

*Giới hạn bộ nhớ: 512 MB*

*Một cây k-phân đầy đủ gồm h tầng sẽ gồm* $\frac{k^{h} - 1}{k - 1}$ *nút
được sinh ra theo cách như sau:*

-   *Tầng thứ nhất chỉ có nút gốc được đánh số 1.*

-   *Xét lần lượt các nút của tầng thứ i theo thứ tự được đánh số, với i
    không quá k - 1, với mỗi nút ta tạo cho nó k nút con được đánh số
    theo thứ tự tăng dần, các nút này sẽ thuộc tầng thứ i + 1. (Ví dụ
    với k = 2 và h = 3: Đầu tiên tạo nút 1, sau đó từ nút 1 tạo ra hai
    nút 2 và 3, từ nút 2 tạo ra hai nút 4 và 5, từ nút 3 tạo ra hai nút
    6 và 7).*

![](media/image5.png){width="6.268055555555556in"
height="1.6527777777777777in"}

*ví dụ về cây tam phân (k = 3) có 4 tầng (h = 4)*

*Trong số các nút của cây, ta đánh dấu các nút*
$p_{1},p_{2},\ldots,\ p_{n}$ *và cần chọn ra số cạnh ít nhất để những
nút này được liên thông với nhau. Bạn hãy xác định số cạnh ít nhất cần
chọn.*

*Input:*

-   *Dòng đầu tiên là các số nguyên k, h, n.*

-   *Dòng thứ hai chứa các số nguyên* $p_{1},p_{2},\ldots,\ p_{n}$*. Dữ
    liệu đầu vào đảm bảo* $p_{i} \neq p_{j}$ *với mọi* $i \neq j$*.*

*Output: Ghi ra số cạnh ít nhất cần chọn.*

*Giới hạn:*
$2 \leq k \leq 10,\ 2 \leq h \leq 18,\ 2 \leq n \leq 5 \times 10^{5},\ 1 \leq p_{i} \leq k^{h}$*.*

*Ví dụ*

+-----------------------------------+-----------------------------------+
| ***Input***                       | ***Output***                      |
+===================================+===================================+
| *3 4 5*                           | *8*                               |
|                                   |                                   |
| *12 13 14 15 16*                  |                                   |
+-----------------------------------+-----------------------------------+
