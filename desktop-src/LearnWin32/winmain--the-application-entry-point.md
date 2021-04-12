---
title: WinMain el punto de entrada de la aplicación
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270903"
---
# <a name="winmain-the-application-entry-point"></a>WinMain: el punto de entrada de la aplicación

Cada programa de Windows incluye una función de punto de entrada que se denomina **WinMain** o **wWinMain**. Esta es la firma de **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Los cuatro parámetros son:

-   *hInstance* es algo denominado "identificador de una instancia" o "identificador de un módulo". El sistema operativo usa este valor para identificar el archivo ejecutable (EXE) cuando se carga en la memoria. El identificador de instancia es necesario para ciertas funciones de Windows, por ejemplo, para cargar iconos o mapas de bits.
-   *hPrevInstance* no tiene ningún significado. Se usaba en Windows de 16 bits, pero ahora siempre es cero.
-   *pCmdLine* contiene los argumentos de la línea de comandos como una cadena Unicode.
-   *nCmdShow* es una marca que indica si la ventana de la aplicación principal se minimizará, maximizará o se mostrará normalmente.

La función devuelve un valor **int** . El sistema operativo no utiliza el valor devuelto, pero puede usar el valor devuelto para transmitir un código de estado a algún otro programa que escriba.

**WINAPI** es la Convención de llamada. Una *Convención de llamada* define cómo una función recibe parámetros del llamador. Por ejemplo, define el orden en que aparecen los parámetros en la pila. Solo tiene que asegurarse de declarar la función **wWinMain** como se muestra.

La función **WinMain** es idéntica a **wWinMain**, salvo que los argumentos de la línea de comandos se pasan como una cadena ANSI. Se prefiere la versión Unicode. Puede utilizar la función de ANSI **WinMain** incluso si compila el programa como Unicode. Para obtener una copia Unicode de los argumentos de la línea de comandos, llame a la función [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) . Esta función devuelve todos los argumentos en una sola cadena. Si desea los argumentos como una matriz de estilo *argv*, pase esta cadena a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

¿Cómo sabe el compilador que debe invocar **wWinMain** en lugar de la función **principal** estándar? Lo que sucede en realidad es que la biblioteca en tiempo de ejecución de Microsoft C (CRT) proporciona una implementación de **Main** que llama a **WinMain** o **wWinMain**.

> [!Note]  
> CRT realiza algunas tareas adicionales en **Main**. Por ejemplo, se llama a cualquier inicializador estático antes de **wWinMain**. Aunque puede indicar al enlazador que use una función de punto de entrada diferente, utilice el valor predeterminado si se vincula a CRT. De lo contrario, se omitirá el código de inicialización de CRT, con resultados imprevisibles. (Por ejemplo, los objetos globales no se inicializarán correctamente).

 

Esta es una función **WinMain** vacía.


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Ahora que tiene el punto de entrada y comprende algunas de las convenciones básicas de codificación y terminología, está listo para crear un programa de ventana completo.

## <a name="next"></a>Siguientes

[Módulo 1. Su primer programa de Windows](your-first-windows-program.md).

 

 