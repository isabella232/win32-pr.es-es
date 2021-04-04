---
title: Tablas de aceleradores
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077762"
---
# <a name="accelerator-tables"></a>Tablas de aceleradores

Las aplicaciones a menudo definen los métodos abreviados de teclado, como CTRL + O para el comando Abrir archivo. Puede implementar los métodos abreviados de teclado mediante el control de mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) individuales, pero las tablas de aceleradores proporcionan una mejor solución que:

-   Requiere menos codificación.
-   Consolida todos los accesos directos en un archivo de datos.
-   Admite la localización en otros idiomas.
-   Permite que los accesos directos y los comandos de menú usen la misma lógica de aplicación.

Una *tabla de aceleradores* es un recurso de datos que asigna combinaciones de teclado, como Ctrl + O, a comandos de la aplicación. Antes de que podamos ver cómo usar una tabla de aceleradores, necesitamos una introducción rápida a los recursos. Un *recurso* es un BLOB de datos integrado en un archivo binario de la aplicación (exe o dll). Los recursos almacenan los datos que necesita la aplicación, como menús, cursores, iconos, imágenes, cadenas de texto o cualquier dato de aplicación personalizado. La aplicación carga los datos de recursos desde el archivo binario en tiempo de ejecución. Para incluir recursos en un archivo binario, haga lo siguiente:

1.  Cree un archivo de definición de recursos (. RC). Este archivo define los tipos de recursos y sus identificadores. El archivo de definición de recursos puede incluir referencias a otros archivos. Por ejemplo, un recurso de icono se declara en el archivo. rc, pero la imagen de icono se almacena en un archivo independiente.
2.  Use el compilador de recursos de Microsoft Windows (RC) para compilar el archivo de definición de recursos en un archivo de recursos compilado (. res). El compilador RC se proporciona con Visual Studio y también el Windows SDK.
3.  Vincule el archivo de recursos compilado al archivo binario.

Estos pasos son aproximadamente equivalentes al proceso de compilación y vinculación de archivos de código. Visual Studio proporciona un conjunto de editores de recursos que facilitan la creación y modificación de recursos. (Estas herramientas no están disponibles en las ediciones Express de Visual Studio). Pero un archivo. RC es simplemente un archivo de texto y la sintaxis se documenta en MSDN, por lo que es posible crear un archivo. RC con cualquier editor de texto. Para obtener más información, consulte [acerca de los archivos de recursos](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definir una tabla de aceleradores

Una tabla de aceleradores es una tabla de métodos abreviados de teclado. Cada acceso directo se define mediante:

-   Identificador numérico. Este número identifica el comando de aplicación que se invocará mediante el acceso directo.
-   Carácter ASCII o código de tecla virtual del acceso directo.
-   Teclas modificadoras opcionales: ALT, Mayús o CTRL.

La tabla de aceleradores tiene un identificador numérico, que identifica la tabla en la lista de recursos de la aplicación. Vamos a crear una tabla de aceleradores para un programa de dibujo sencillo. Este programa tendrá dos modos: modo de dibujo y modo de selección. En el modo Draw, el usuario puede dibujar formas. En el modo de selección, el usuario puede seleccionar formas. Para este programa, nos gustaría definir los siguientes métodos abreviados de teclado.



| Acceso directo | Get-Help                   |
|----------|---------------------------|
| CTRL+M   | Alterna entre los modos.     |
| F1       | Cambiar al modo de dibujo.      |
| F2       | Cambiar al modo de selección. |



 

En primer lugar, defina los identificadores numéricos para la tabla y los comandos de la aplicación. Estos valores son arbitrarios. Puede asignar constantes simbólicas para los identificadores al definirlas en un archivo de encabezado. Por ejemplo:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



En este ejemplo, el valor `IDR_ACCEL1` identifica la tabla de aceleradores y las tres constantes siguientes definen los comandos de la aplicación. Por Convención, un archivo de encabezado que define las constantes de recursos se denomina a menudo Resource. h. La siguiente lista muestra el archivo de definición de recursos.


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

-   Código de tecla virtual o carácter ASCII que invoca el acceso directo.
-   El comando de aplicación. Observe que se utilizan constantes simbólicas en el ejemplo. El archivo de definición de recursos incluye Resource. h, donde se definen estas constantes.
-   La palabra clave **VIRTKEY** significa que la primera entrada es un código de clave virtual. La otra opción es usar caracteres ASCII.
-   Modificadores opcionales: ALT, CONTROL o SHIFT.

Si usa caracteres ASCII para los accesos directos, un carácter en minúsculas será un método abreviado diferente que un carácter en mayúsculas. (Por ejemplo, escribir ' a ' puede invocar un comando diferente que escribir ' A '). Esto puede confundir a los usuarios, por lo que suele ser mejor usar códigos de tecla virtual, en lugar de caracteres ASCII, para los accesos directos.

## <a name="loading-the-accelerator-table"></a>Cargar la tabla de aceleradores

El recurso de la tabla de aceleradores debe cargarse antes de que el programa pueda usarlo. Para cargar una tabla de aceleradores, llame a la función [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Llame a esta función antes de escribir el bucle de mensajes. El primer parámetro es el identificador del módulo. (Este parámetro se pasa a la función [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) . Para obtener más información, vea [WinMain: el punto de entrada de la aplicación](winmain--the-application-entry-point.md)). El segundo parámetro es el identificador de recursos. La función devuelve un identificador al recurso. Recuerde que un identificador es un tipo opaco que hace referencia a un objeto administrado por el sistema. Si se produce un error en la función, devuelve **null**.

Puede liberar una tabla de aceleradores llamando a [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). Sin embargo, el sistema libera automáticamente la tabla cuando el programa finaliza, por lo que solo necesita llamar a esta función si está reemplazando una tabla por otra. Hay un ejemplo interesante de esto en el tema [creación de aceleradores editables](/windows/desktop/menurc/using-keyboard-accelerators)por el usuario.

## <a name="translating-key-strokes-into-commands"></a>Traducir los trazos de tecla en comandos

Una tabla de aceleradores funciona traduciendo los trazos clave en mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) . El parámetro *wParam* del **\_ comando WM** contiene el identificador numérico del comando. Por ejemplo, con la tabla mostrada anteriormente, el trazo de tecla CTRL + M se convierte en un mensaje de **\_ comando de WM** con el valor `ID_TOGGLE_MODE` . Para que esto suceda, cambie el bucle de mensajes a lo siguiente:


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



Este código agrega una llamada a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) dentro del bucle de mensajes. La función **TranslateAccelerator** examina cada mensaje de ventana, buscando mensajes de tecla presionada. Si el usuario presiona una de las combinaciones de teclas enumeradas en la tabla de aceleradores, **TranslateAccelerator** envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) a la ventana. La función envía **un \_ comando de WM** mediante la invocación directa del procedimiento de ventana. Cuando **TranslateAccelerator** traduce correctamente un trazo de clave, la función devuelve un valor distinto de cero, lo que significa que debe omitir el procesamiento normal del mensaje. De lo contrario, **TranslateAccelerator** devuelve cero. En ese caso, pase el mensaje de ventana a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), como es habitual.

Este es el modo en que el programa de dibujo podría controlar el mensaje del [**\_ comando de WM**](/windows/desktop/menurc/wm-command) :


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



En este código se supone que `SetMode` es una función definida por la aplicación para cambiar entre los dos modos. Los detalles de cómo controlar cada comando obviamente dependen de su programa.

## <a name="next"></a>Siguientes

[Establecer la imagen del cursor](setting-the-cursor-image.md)

 

 