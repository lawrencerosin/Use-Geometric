# Use-Geometric
Shows the nfo of multiple shapes using regular classes, an abstract class, and an interface
public interface SidedObject {
    int GetSideAmount();
}
public abstract class GeometricFigure2 implements SidedObject{
    private int width, height;
    private String figureType;
    public GeometricFigure2(int Width, int Height, String FigureType)
    {
        width=Width;
        height=Height;
        figureType=FigureType;
    }
    public abstract double FindArea();
    public int GetWidth()
    {
        return width;
    }
    public int GetHeight()
    {
        return height;
    }
    public String GetFigureType()
    {
        return figureType;
    }
}
public class Square2 extends GeometricFigure2 implements SidedObject{
    private int sides;
    public Square2(int width)
    {   //Since the height and width of a square must be the same
        super(width, width, "Square");
        sides=GetSideAmount();
    }
    public double FindArea()
    {
        int area=GetWidth()*GetHeight();
        return area;
    }
    public int GetSideAmount()
    {
        return 4;
    }
    public int GetSides()
    {
        return sides;
    }
    
}
public class Triangle2 extends GeometricFigure2{
    private int sides;
    public Triangle2(int width, int height)
    {
        super(width, height, "Triangle");
    }
    public double FindArea()
    {
        double area;
        area=(double)GetWidth()*GetHeight()/2;
        return area;
    }
    public int GetSideAmount()
    {
        return 3;
    }
    public int GetSides()
    {
        return sides;
    }
}

