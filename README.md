# code-h9.2
import java.util.Locale;
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Mời bạn nhập Họ và Tên: ");
        String fullname = scanner.nextLine();
        String[] arrname = fullname.split("\\s+");
        StringBuilder HoTenVietHoa = new StringBuilder();
        for (String name : arrname)
        {
            if (name.length() > 0)
            {
                HoTenVietHoa.append(name.substring(0, 1).toUpperCase());
                HoTenVietHoa.append(name.substring(1).toLowerCase());
                HoTenVietHoa.append(" ");
            }
        }
        System.out.println("Họ và tên của bạn là: " + HoTenVietHoa);
        String[] sentences = {
                "Đầu long hai ả tố nga.",
                "Thúy Kiều là chị, em là Thúy Vân.",
                "Mai cốt cách, tuyết tinh thần,",
                "Mỗi nguời một vẻ, mười phân vẹn mười.",
                "Vân xem trang trọng khác vời,",
                "Khuôn trăng đầy đặn, nét ngài nở nang.",
                "Hoa cười nhọc thôt đoan trang,",
                "Mây thua nước tóc, tuyết nhường màu da.",
        };

        int indentSize = 0;
        for (int i = 0; i < sentences.length; i++)
        {
            if (i < sentences.length - 1 && sentences[i].length() < sentences[i + 1].length())
            {
                indentSize += 4;
            }
            else
            {
                indentSize = 0;
            }

            for (int j = 0; j < indentSize; j++)
            {
                System.out.print(" ");
            }

            System.out.print(sentences[i] +"\n");
        }

    }
}
