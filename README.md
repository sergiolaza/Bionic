package vect;

/**
 * 
 * Represents Vectors
 *
 */
public class Vector3D {
	/**
	 * @param x - vector’s coordinate
	 *             
	 * @param y- vector’s coordinate
	 *             
	 * @param z - vector’s coordinate
	 *            
	 */
	double x, y, z;

	/**
	 * Default constructor sets vector’s coordinates zero
	 * 
	 */
	public Vector3D() {
		// TODO Auto-generated constructor stub
	}
	/**
	 * Initialized vector’s coordinates
	 * 
	 */
	public Vector3D(double x, double y, double z) {
		// TODO Auto-generated constructor stub

		this.x = x;
		this.y = y;
		this.z = z;
	}

	public double getX() {
		return x;
	}

	public void setX(int x) {
		this.x = x;
	}

	public double getY() {
		return y;
	}

	public void setY(int y) {
		this.y = y;
	}

	public double getZ() {
		return z;
	}

	public void setZ(int z) {
		this.z = z;
	}

	/**
	 * Returns a new Vector that is a sum of this vector with a parameter
	 * @param vect- summand           
	 * @return vector that is the sum of two vectors
	 * 
	 */
	public Vector3D addVector(Vector3D vect) {

		double x = this.x + vect.getX();
		double y = this.y + vect.getY();
		double z = this.z + vect.getZ();
		return new Vector3D(x, y, z);

	}

	/**
	 * Returns a new Vector that is a product of this vector and a parameter 
	 * @param vect - multiplier            
	 * @return a specified product
	 * 
	 */
	public Vector3D multiplyVector(Vector3D vect) {

		double x = this.y * vect.getZ() - this.z * vect.getY();
		double y = this.z * vect.getX() - this.x * vect.getZ();
		double z = this.x * vect.getY() - this.y * vect.getX();
		return new Vector3D(x, y, z);

	}

	/**
	 * Returns scalar product this vector and a parameter 
	 * @param v1 - scalar multiplier
	 * @return a specified scalar product
	 * 
	 */
	public double calcScalar(Vector3D v1) {

		return v1.getX() * this.x + v1.getY() * this.y + v1.getZ() * this.z;

	}

	/**
	 * Returns result of calculate a module
	 * @return a specified module
	 * 
	 */
	public double calcModule() {
		return Math.sqrt(x * x + y * y + z * z);

	}

}
