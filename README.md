# TugasOPPPertemuan7

* Nama : Doni Perdana Siringoringo
* NIM  : 312210687
* Kelas: TI.22.B1

### Berikut menampilkan *SETTER* dan *GETTER* gaji pegawai, progammer dan manager

### Berikut Source code

    --public class Pegawai
--{


    private string nama;
    private double gajiPokok;

    public void setNama(string nama)
    {
        this.nama = nama;
    }
    public string getNama() { return this.nama; }

    public double getGajiPokok() { return this.gajiPokok; }

    public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

    public void cetakinfo()
    {

        Console.WriteLine("Nama : " + this.nama);
        Console.WriteLine("Gapok : " + this.gajiPokok);
    }
}


public class manager : Pegawai
{

    private double tunjangan;

    public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
    public double getTunjangan() { return this.tunjangan; }

    public new void cetakinfo()
    {

        base.cetakinfo();
        this.cetakTunjangan();
    }
    public void cetakTunjangan()
    {
        Console.WriteLine("Tunjangan Anda : " + this.tunjangan);

    }
}

public class Programmer : Pegawai
{
    private double bonus;


    public void setBonus(double bonus) { this.bonus = bonus; }

    public double getBonus() { return this.bonus; }

    public new void cetakinfo()
    {
        base.cetakinfo();
        this.cetakBonus();
    }
    public void cetakBonus()
    {
        Console.WriteLine("Bonus : " + this.bonus);


    }

}
class program
{
    static void Main(string[] args)
    {
        Console.WriteLine("==== PEGAWAI ====");
        Pegawai pegawai = new Pegawai();
        pegawai.setNama("Doni Perdana Siringoringo");
        pegawai.setGajiPokok(6000000);
        pegawai.cetakinfo();
        Console.WriteLine();

        Console.WriteLine("==== MANAGER ====");
        manager Manager = new manager();
        Manager.setNama("Doni Perdana Siringoringo");
        Manager.setGajiPokok(2000000);
        Manager.setTunjangan(8000000);
        Manager.cetakinfo();
        Console.WriteLine();

        Console.WriteLine("==== PROGRAMMER ====");
        Programmer programer = new Programmer();
        programer.setNama("Doni Perdana Siringoringo");
        programer.setGajiPokok(15000000);
        programer.setBonus(7000000);
        programer.cetakinfo();
        Console.WriteLine();


        Console.WriteLine("press anykey");
        Console.ReadKey();
    }
 }--
 Berikut Hasil Output nya

 
 ![Screenshot (612)](https://github.com/Doniprs/TugasOPPPertemuan7/assets/115882455/f6652277-52fd-4af9-a831-0bad5ab75cd6)

