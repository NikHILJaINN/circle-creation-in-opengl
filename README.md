# circle-creation-in-opengl

#include <GL/glut.h>
#include <math.h>
void display()
{
glClear(GL_COLOR_BUFFER_BIT);
glColor3f(0,1,0);
glBegin(GL_POLYGON);
glVertex2f(-0.6,0.7); // center of circle
for(int i = 0; i <= 20;i++) 
glVertex2f(-0.6 + (0.1 * cos(i *  2.0f * 3.14 / 20)), 0.7 + (0.1 * sin(i * 2.0f * 3.14 / 20)));
glEnd();
glColor3f(1,1,1);
glRasterPos2f(-0.70,-0.70);
glutBitmapString(GLUT_BITMAP_HELVETICA_18,"NIKHIL JAIN");
glFlush();
}
int main(int argc,char** argv)
{
glutInit(&argc,argv);
glutInitDisplayMode(GLUT_SINGLE|GLUT_RGB);
glutInitWindowSize(900,900);
glutInitWindowPosition(300,500);
glutCreateWindow(" green triangle");
glClearColor(1,0,0,1);
glutDisplayFunc(display);
glutMainLoop();
return 0;
}
