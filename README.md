# estructuras
#include <iostream>
#include <conio.h>

using namespace std;
struct direccion
{
    char calle[20];
    int cp;
    char ciudad[20];
};
struct persona
{
    char nombre[20];
    int edad;
    structdireccion dire;
};

int main(int argc, char** argv)
{
    struct persona P1[5];
    struct persona *apuntador;

    apuntador=&P1[0];

    for(int i=0; i<2;i++)
    {
        cout<<"nombre: ";
        cin.getline(P1[i].nombre,20,'\n');
        cout<<"Edad: ";
        cin>>P1[i].edad;
        cout<<"Estatura: ";
        cin>>P1[i].estatura;
        cout<<"calle: ";
        fflush(stdin);
        cin.getline(P1[i].dire.calle,20 '\n');
    }

    cout<<endl<<"nombre guardado: "<<apuntador->nombre;
    cout<<endl<<"edad guardada: "<<apuntador->edad;
    cout<<endl<<"estatura guardada: "<<apuntador->estatura;
    cout<<endl<<"calle guardda: "apuntador->dire.calle;
    getch();
    return 0;
}
