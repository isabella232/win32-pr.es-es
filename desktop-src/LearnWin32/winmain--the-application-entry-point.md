---
title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018
---

# <a name="winmain-the-application-entry-point"></a>WinMain: el punto de entrada de la aplicación

Cada programa de Windows incluye una función de punto de entrada denominada **WinMain** o **wWinMain**. Esta es la firma de **wWinMain.**


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Los cuatro parámetros son:

-   *hInstance* es algo denominado "identificador de una instancia" o "identificador de un módulo". El sistema operativo usa este valor para identificar el ejecutable (EXE) cuando se carga en memoria. El identificador de instancia es necesario para determinadas funciones de Windows, por ejemplo, para cargar iconos o mapas de bits.
-   *hPrevInstance* no tiene ningún significado. Se usó en Windows de 16 bits, pero ahora es siempre cero.
-   *pCmdLine contiene* los argumentos de línea de comandos como una cadena Unicode.
-   *nCmdShow* es una marca que indica si la ventana principal de la aplicación se minimizará, maximizará o se mostrará con normalidad.

La función devuelve un **valor** int. El sistema operativo no usa el valor devuelto, pero puede usar el valor devuelto para transmitir un código de estado a algún otro programa que escriba.

**WINAPI** es la convención de llamada. Una *convención de llamada* define cómo una función recibe parámetros del autor de la llamada. Por ejemplo, define el orden en que aparecen los parámetros en la pila. Asegúrese de declarar la función **wWinMain** como se muestra.

La **función WinMain** es idéntica a **wWinMain,** salvo que los argumentos de la línea de comandos se pasan como una cadena ANSI. Se prefiere la versión Unicode. Puede usar la función **ANSI WinMain** incluso si compila el programa como Unicode. Para obtener una copia Unicode de los argumentos de la línea de comandos, llame a la [**función GetCommandLine.**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) Esta función devuelve todos los argumentos de una sola cadena. Si desea que los argumentos como una *matriz argv*-style, pase esta cadena a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

¿Cómo sabe el compilador invocar **wWinMain en** lugar de la **función main** estándar? Lo que sucede realmente es que la biblioteca en tiempo de ejecución de Microsoft C (CRT) proporciona una implementación de **main** que llama a **WinMain** o **wWinMain**.

> [!Note]  
> CRT realiza algún trabajo adicional dentro de **main**. Por ejemplo, se llama a cualquier inicializador estático antes **que wWinMain**. Aunque puede decir al vinculador que use una función de punto de entrada diferente, use el valor predeterminado si vincula a CRT. De lo contrario, se omitirá el código de inicialización de CRT, con resultados imprevisibles. (Por ejemplo, los objetos globales no se inicializarán correctamente).

 

Esta es una función **vacía de WinMain.**


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Ahora que tiene el punto de entrada y comprende algunas de las convenciones básicas de terminología y codificación, está listo para crear un programa de Ventana completo.

## <a name="next"></a>Siguientes

[Módulo 1. Su primer programa de Windows.](your-first-windows-program.md)

 

 
