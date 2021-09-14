---
title: Tablas de aceleradores
description: Tablas de aceleradores
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160012"
---
# <a name="accelerator-tables"></a>Tablas de aceleradores

Las aplicaciones suelen definir métodos abreviados de teclado, como CTRL+O para el comando Abrir archivo. Puede implementar métodos abreviados de teclado mediante el control de mensajes [**DE WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) individuales, pero las tablas de aceleradores proporcionan una solución mejor que:

-   Requiere menos codificación.
-   Consolida todos los accesos directos en un archivo de datos.
-   Admite la localización en otros idiomas.
-   Permite que los métodos abreviados y los comandos de menú usen la misma lógica de aplicación.

Una *tabla de aceleradores* es un recurso de datos que asigna combinaciones de teclado, como CTRL+O, a los comandos de aplicación. Antes de ver cómo usar una tabla de aceleradores, necesitamos una introducción rápida a los recursos. Un *recurso* es un blob de datos integrado en un archivo binario de aplicación (EXE o DLL). Los recursos almacenan los datos necesarios para la aplicación, como menús, cursores, iconos, imágenes, cadenas de texto o cualquier dato de aplicación personalizado. La aplicación carga los datos de recursos del archivo binario en tiempo de ejecución. Para incluir recursos en un archivo binario, haga lo siguiente:

1.  Cree un archivo de definición de recursos (.rc). Este archivo define los tipos de recursos y sus identificadores. El archivo de definición de recursos puede incluir referencias a otros archivos. Por ejemplo, un recurso de icono se declara en el archivo .rc, pero la imagen de icono se almacena en un archivo independiente.
2.  Use microsoft Windows Resource Compiler (RC) para compilar el archivo de definición de recursos en un archivo de recursos compilado (.res). El compilador RC se proporciona con Visual Studio y también el SDK Windows.
3.  Vincule el archivo de recursos compilado al archivo binario.

Estos pasos son aproximadamente equivalentes al proceso de compilación o vínculo para los archivos de código. Visual Studio proporciona un conjunto de editores de recursos que facilita la creación y modificación de recursos. (Estas herramientas no están disponibles en las ediciones Express de Visual Studio). Pero un archivo .rc es simplemente un archivo de texto y la sintaxis se documenta en MSDN, por lo que es posible crear un archivo .rc mediante cualquier editor de texto. Para obtener más información, vea [Acerca de los archivos de recursos](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definir una tabla de aceleradores

Una tabla de aceleradores es una tabla de métodos abreviados de teclado. Cada acceso directo se define mediante:

-   Identificador numérico. Este número identifica el comando de aplicación que invocará el acceso directo.
-   El carácter ASCII o el código de clave virtual del acceso directo.
-   Teclas modificadoras opcionales: ALT, MAYÚS o CTRL.

La propia tabla de aceleradores tiene un identificador numérico, que identifica la tabla en la lista de recursos de la aplicación. Vamos a crear una tabla de aceleradores para un sencillo programa de dibujo. Este programa tendrá dos modos: modo de dibujo y modo de selección. En el modo de dibujo, el usuario puede dibujar formas. En el modo de selección, el usuario puede seleccionar formas. Para este programa, nos gustaría definir los siguientes métodos abreviados de teclado.



| Acceso directo | Comando                   |
|----------|---------------------------|
| CTRL+M   | Alternar entre modos.     |
| F1       | Cambie al modo de dibujo.      |
| F2       | Cambie al modo de selección. |



 

En primer lugar, defina identificadores numéricos para la tabla y para los comandos de aplicación. Estos valores son arbitrarios. Puede asignar constantes simbólicas para los identificadores si las define en un archivo de encabezado. Por ejemplo:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



En este ejemplo, el valor identifica la tabla de aceleradores y las tres `IDR_ACCEL1` constantes siguientes definen los comandos de aplicación. Por convención, un archivo de encabezado que define las constantes de recursos a menudo se denomina resource.h. En la lista siguiente se muestra el archivo de definición de recursos.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



Los métodos abreviados de acelerador se definen dentro de las llaves. Cada acceso directo contiene las siguientes entradas.

-   Código de clave virtual o carácter ASCII que invoca el acceso directo.
-   Comando de aplicación. Observe que en el ejemplo se usan constantes simbólicas. El archivo de definición de recursos incluye resource.h, donde se definen estas constantes.
-   La palabra **clave VIRTKEY** significa que la primera entrada es un código de clave virtual. La otra opción es usar caracteres ASCII.
-   Modificadores opcionales: ALT, CONTROL o MAYÚS.

Si usa caracteres ASCII para los accesos directos, un carácter en minúscula será un acceso directo diferente de un carácter en mayúsculas. (Por ejemplo, escribir "a" podría invocar un comando diferente al de "A"). Esto podría confundir a los usuarios, por lo que suele ser mejor usar códigos de clave virtual, en lugar de caracteres ASCII, para los accesos directos.

## <a name="loading-the-accelerator-table"></a>Carga de la tabla de aceleradores

El recurso de la tabla de aceleradores debe cargarse antes de que el programa pueda usarlo. Para cargar una tabla de aceleradores, llame [**a la función LoadAccelerators.**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa)


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Llame a esta función antes de escribir el bucle de mensajes. El primer parámetro es el identificador del módulo. (Este parámetro se pasa a la [**función WinMain.**](/windows/desktop/api/winbase/nf-winbase-winmain) Para más información, consulte [WinMain: el punto de entrada de la aplicación).](winmain--the-application-entry-point.md) El segundo parámetro es el identificador de recurso. La función devuelve un identificador al recurso. Recuerde que un identificador es un tipo opaco que hace referencia a un objeto administrado por el sistema. Si se produce un error en la función, devuelve **NULL.**

Puede liberar una tabla de aceleradores llamando a [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). Sin embargo, el sistema libera automáticamente la tabla cuando se cierra el programa, por lo que solo tiene que llamar a esta función si va a reemplazar una tabla por otra. Hay un ejemplo interesante de esto en el tema Creación de [aceleradores editables de usuario](/windows/desktop/menurc/using-keyboard-accelerators).

## <a name="translating-key-strokes-into-commands"></a>Traducción de trazos clave en comandos

Una tabla de aceleradores funciona mediante la traducción de trazos de teclas en [**mensajes \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) El *parámetro wParam* de **WM \_ COMMAND** contiene el identificador numérico del comando. Por ejemplo, mediante la tabla mostrada anteriormente, el trazo de tecla CTRL+M se traduce en un **mensaje WM \_ COMMAND** con el valor `ID_TOGGLE_MODE` . Para que esto suceda, cambie el bucle de mensajes a lo siguiente:


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



Este código agrega una llamada a la [**función TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) dentro del bucle de mensajes. La **función TranslateAccelerator** examina cada mensaje de ventana y busca mensajes de tecla abajo. Si el usuario presiona una de las combinaciones de teclas enumeradas en la tabla de aceleradores, **TranslateAccelerator** envía un [**mensaje WM \_ COMMAND**](/windows/desktop/menurc/wm-command) a la ventana. La función envía **WM \_ COMMAND** invocando directamente el procedimiento de ventana. Cuando **TranslateAccelerator** traduce correctamente un trazo de clave, la función devuelve un valor distinto de cero, lo que significa que debe omitir el procesamiento normal del mensaje. De lo contrario, **TranslateAccelerator** devuelve cero. En ese caso, pase el mensaje de ventana [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), como de forma normal.

Este es el modo en que el programa de dibujo podría controlar el [**mensaje \_ WM COMMAND:**](/windows/desktop/menurc/wm-command)


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



Este código supone que es una función definida por la `SetMode` aplicación para cambiar entre los dos modos. Obviamente, los detalles de cómo controlaría cada comando dependen del programa.

## <a name="next"></a>Siguientes

[Establecimiento de la imagen de cursor](setting-the-cursor-image.md)

 

 
