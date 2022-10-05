# Solar-System
Solar system is a set of celestial bodies bound by gravitational forces. The movement of celestial bodies  like the sun, stars, planets and the other will be more easily understood if taught through visualization movement  through computer animation. This visualization shows the solar system planetary motion, or we can call it a  revolution, that is, when the planets move around the sun, and remain in orbit each using OpenGL API to represent  the solar system as a visual.
# The sun is drawn by using the following lines of code. 
{ 
glPushMatrix(); 
glRotatef(…); 
glLightfv(GL_LIGHT0,GL_POSITION,position); 
glDisable(GL_LIGHTING); 
glutSolidSphere(…); 
glPopMatrix(); 
}

# The planets Saturn and Uranus are the 2 planets in our solar system with rings. 
They are implemented using the following codes. 
{ 
glPushMatrix(); 
glRotatef(…); 
glTranslatef(…); 
gluLookAt(0.0,10.0,2.0,1.0,0.0,0.0,0.0,0.0,1.0); 
glutSolidSphere(…); 
int i=0; 
glBegin(GL_QUAD_STRIP); 
for(i=0;i<=360;i++) 
{ 
glVertex3f(sin(i*3.1416/180)*0.5,cos(i*3.1416/180)*0.5,0); 
glVertex3f(sin(i*3.1416/180)*0.7,cos(i*3.1416/180)*0.7,0); 
} glEnd(); 
glPopMatrix(); 
}

# The earth is drawn along with its natural satellite, moon which revolve round the earth. The 
following lines of codes are used to implement the earth and the moon. 
{ 
glPushMatrix(); 
glRotatef(…); 
glTranslatef(…); 
glRotatef(…); 
glColor3f(…); 
glutSolidSphere(…); /*draw planet earth*/ 
Celestial Exploratory
 
Department of CSE, SJCIT 14 2021-2022 
glRotatef(…); 
glTranslatef(…); 
glColor3f(…); 
glutSolidSphere(…); /*draw moon*/ 
glPopMatrix();

#  The remaining planets are Mercury, Venus, Mars, Jupiter and Neptune. All 
these planets are implemented using the same set of codes by changing the values and colors. 
{ 
glPushMatrix(); 
glRotatef(…); 
glTranslatef(…); 
glRotatef(…); 
glColor3f(…); 
glutSolidSphere(…); /*draw smaller planet mercury*/ 
glPopMatrix(); 
}

# The comet is made to revolve round the sun. 
The following codes are used to implement the comet. 
{ 
glPushMatrix(); 
glRotatef((GLfloat)c,6.0,-14.0,-6.0); 
glTranslatef(5.0,3.0,-1.0); 
glScalef(0.60,0.0,2.5); 
glColor3f(7.5,9.5,2.0); 
glutSolidSphere(0.2,12,6); /*draw comet*/ 
glPopMatrix(); 
}

#
