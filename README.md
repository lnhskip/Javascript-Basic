# Javascript Basic

## Một số hàm built-in(Là những hàm được xây dựng sẵn)
1. Alert
    -  Show ra cảnh báo trên trình duyệt
    - Vd: alert("Hello world!!!")
2. Console
    - Là đối tượng gồm các phương thức để giao tiếp với trình console của browser
    - Vd: console.log("Nguyen Duy Linh")
3. Confirm
    - Show ra hộp thoại để xác nhận, với message là giá trị truyền vào
    - Vd: confirm("Bạn chắc chắn muốn học javascript chứ?")
4. Prompt
    - Show ra hộp thoại có thể nhập giá trị trên đó, với message là giá trị truyền vào
    - Vd: prompt("Nhập số tuổi")
5. Set timeout
    - Set thời gian sau bao lâu để xử lý một công việc, với tham số truyền vào là milisecond 
    - Vd: setTimeout( function () {
          console.log("Đây là message được show ra sau 1s")
      }, 1000 )
6. Set interval
    - Thực hiện một công việc lặp đi lặp lại sau một khoảng thời gian, với tham số truyền vào là milisecond
    - Vd: setInterval( function () {
          console.log("In ra sau 1s" + Math.random())
      }, 1000 )

## Variables(Biến)
- Có 3 cách khai báo biến trong javascript: var, let, const
- var - cách sử dụng
    ```
        // var - có thể khai báo theo 2 cách:
        var number = 1;
        number2 = 2;

        // có thể gán lại giá trị theo cách sau
        var number = 3;
        number = 5;

        // Nếu biến được sử dụng trước khi khởi tạo sẽ được hiểu là undefined
        console.log(phone); // kết quả show ra là undefined
        phone = 0999899999;
    ```
- let - giống với var nhưng cách sử dụng sẽ khắt khe hơn
    ```
        // Có một số lưu ý khi sử dụng let
        // Không thể gán lại giá trị bằng từ khóa let
        let age = 24;
        let age = 30; // sẽ báo lỗi syntax error trên console
        age = 30; // hợp lệ

        // Phải được khai báo trước khi sử dụng
        console.log(name); // Xảy ra lỗi không thể truy cập
        let name = "Nguyen Duy Linh";
    ```

- const - biến được khai báo với const sẽ không thể thay đổi giá trị của nó
    ```
        const PI = 3.1415926;
        PI = 2; // Xảy ra lỗi
    ```

## Kiểu dữ liệu(Data type)
1. Dữ liệu nguyên thủy - Primitive data type
    - Number
    - String
    - Boolean
    - Undefined
    - Null
    - Symbol
2. Dữ liệu phức tạp - Complex data type
    - Function
    - Object

- Trong javascript kiểu dữ liểu của biến sẽ được định nghĩa bởi giá trị sau dấu bằng

    ```
      // Kiểu number
      var x = 1;
      var y = 1.5;

      // Kiểu string
      // Có 2 cách khai báo
      var name = "Linh";
      var fullName = new String("Nguyen Duy Linh");

      // Kiểu boolean
      var isChecked = true;

      // Kiểu undefined;
      var age;

      // Kiểu null
      var isNull = null;

      // Kiểu symbol
      var id = Symbol('id'); // unique

      // Kiểu object
      var myObject = {
        name: Linh,
        age: 24,
        myFunction: function () {

        }
      };

      // Kiểu function
      var myFunction = function() {
        alert("Nguyen Duy Linh");
      }

      // Sử dụng typeOf để kiểm tra kiểu dữ liệu
      var x = 1;
      typeOf x;
    ```

## Operator(Toán tử)
- Toán tử số học - Arithmetic

    -- Trừ(-)

        var subtraction = 16 - 10;
        
    -- Cộng(+)

        var addition = 16 + 10;

        // Chú ý:
        // Nếu cộng hai biến mà một trong 2 biến là chuỗi thì toán tử sẽ là toán tử nối chuỗi
        var name = Linh;
        var age = 24;
        console.log(name + age) // Hiển thị Linh24
        
    -- Nhân(*)

        var multiplication = 16 * 10;
        
    -- Chia(/)

        var division = 10 / 2;
        
    -- Chia lấy phần nguyên(%)

        var modulus = 10 % 3;

        
    -- Tăng lên 1(++)

        var increment = 10;
        increment++;
        
    -- Giảm đi 1(--)

        var decrement = 10;
        decrement--;

- Toán tử gán - Assignment(=)
  
      ```
      var number = 1;
      number = 2
      ```

- Toán tử so sánh - Comparison

  -- Equal(`==`)

  -- Not Equal(`!=`)

  -- Greater than(`>`)

  -- Less than(`<`)

  -- Greater than or Equal to(`>=`)

  -- Less than or Equal to(`<=`)

  -- Equal value and data type(`===`)

  -- Not equal value and data type(`!==`)

- Toán tử logic

  -- Logical AND(`&&`)

  -- Logical OR(`||`)

  -- Logical NOT(`!`)

## Condition(Điều kiện)
- If - dùng để biểu diễn những hành động khác nhau cho những quyết định khác nhau
    ```
        if (hour > 8.30) {
          console.log("Working");
        }
        else if (hour > 12 && hour < 13)
        {
          console.log("Have lunch");
        }
        else
        {
          console.log("Other");
        }
    ```
    
## Array(Mảng)
- Trong javascript mảng có thể lưu giữ nhiều giá trị và không nhất thiết phải cùng kiểu dữ liệu
    ```
    var languages = [
        "JavaScript",
        "Java",
        "Python",
        null,
        undefined,
        function(){},
        {},
    ];

    // Trong Array thì mọi phần tử đều được đánh chỉ mục và bắt đầu từ 0
    // Cách truy xuất phần tử của mảng theo index
    console.log( language[0] );

    // Cú pháp khai báo mảng
    // Có 2 cách khao báo mảng
    var number = [1, 3, 4, 12]
    var string = new Array( "Nguyen", "Duy", "Linh" );
    ```
- Các phương thức hay được sử dụng trong Array
    - pop - xóa đi phần tử ở cuối mảng và trả về phần tử mà nó đã xóa
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        var language = languages.pop();

        // Chú ý: khi sử dụng pop mà mảng không còn phần tử nào thì kết quả trả về sẽ là undefined
        ```
    - push - chèn một hoặc nhiều phần tử vào cuối mảng và trả về độ dài mới của mảng
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        var length = languages.push("C#", "C++");
        ```
    - shift - xóa đi phần tử ở đầu mảng và trả về phần tử mà nó đã xóa
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        var language = languages.shift();
        ```
    - unshift - chèn một hoặc nhiều phần tử vào đầu mảng và trả về độ dài mới của mảng
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        var length = languages.unshift("C#", "C++");
        ```
    - splicing - Xóa một hoặc nhiều phần tử bất kỳ và thêm phần tử mới
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        // Các tham số truyền vào
        // Tham số đầu tiên: Vị trí đặt con trỏ để xóa
        // Tham số thứ hai: Số phần tử được xóa
        // Tham số còn lại: Các phần tử được chèn
        languages.splice(1, 1, "C#", "C++");
        ```
    - concat - Gộp array
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        var languages2 = [
            "C#",
            "C++",
        ];

        // Mảng languages sẽ cộng thêm hai phần tử từ mảng languages2
        languages.concat(languages2);
        ```
    - slicing - trả về một bản sao của mảng thành một đối tượng mảng mới, gồm các tham số là vị trí phần tử đầu và cuối của mảng
        ```
        var languages = [
            "JavaScript",
            "Java",
            "Python",
        ];

        console.log( languages.slice(1) )
        // Kết quả: Array [ "Java", "Python" ]

        console.log( languages.slice(0, 1) )
        // Kết quả: Array [ "JavaScript", "Java" ]
        ```
