---
title: Cumplimiento estricto
description: Algunos códigos fuente que se compilan correctamente pueden generar mensajes de error cuando se habilita la comprobación estricta de tipos.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420977"
---
# <a name="strict-compliance"></a>Cumplimiento estricto

Algunos códigos fuente que se compilan correctamente pueden generar mensajes de error cuando se habilita la comprobación **estricta** de tipos. En las secciones siguientes se describen los requisitos mínimos para que el código se compile cuando **STRICT** esté habilitado. Se recomiendan pasos adicionales, especialmente para generar código portable.

## <a name="general-requirements"></a>Requisitos generales

El requisito principal es que debe declarar tipos de control y punteros de función correctos en lugar de confiar en tipos más generales. No se puede usar un tipo de identificador en el que se espera otro. Esto también significa que puede que tenga que cambiar las declaraciones de función y utilizar más conversiones de tipos.

Para obtener los mejores resultados, el tipo de **identificador** genérico solo debe usarse cuando sea necesario.

## <a name="declaring-functions-within-your-application"></a>Declarar funciones dentro de la aplicación

Asegúrese de que se declaran todas las funciones de aplicación. Se recomienda colocar todas las declaraciones de función en un archivo de inclusión porque puede examinar fácilmente las declaraciones y buscar los tipos de parámetro y de valor devuelto que se deben cambiar.

Si usa la opción del compilador **/ZG** para crear archivos de encabezado para las funciones, recuerde que obtendrá resultados diferentes en función de si ha habilitado la comprobación **estricta** de tipos. Con **STRICT** deshabilitado, todos los tipos de identificador generan el mismo tipo base. Con **STRICT** habilitado, generan distintos tipos base. Para evitar conflictos, debe volver a crear el archivo de encabezado cada vez que habilite o deshabilite **STRICT**, o edite el archivo de encabezado para usar los tipos **hWnd**, **HDC**, **Handle**, etc., en lugar de los tipos base.

Es posible que las declaraciones de función que copió de Windows. h en el código fuente hayan cambiado y que la declaración local no esté actualizada. Quite la declaración local.

## <a name="types-that-require-casts"></a>Tipos que requieren conversiones

Algunas funciones tienen tipos de valor devueltos o parámetros genéricos. Por ejemplo, la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) devuelve datos que pueden ser cualquier número de tipos, dependiendo del contexto. Cuando vea cualquiera de estas funciones en el código fuente, asegúrese de usar la conversión de tipos correcta y de que sea lo más específica posible. La lista siguiente es un ejemplo de estas funciones.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Al llamar a [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), primero debe convertir el resultado al tipo **uint \_ ptr**. Debe realizar pasos similares para cualquier función que devuelva un valor **LRESULT** o **Long \_ ptr** , donde el resultado contiene un identificador. Esto es necesario para escribir código portable, ya que el tamaño de un identificador varía en función de la versión de Windows. La conversión (**uint \_ ptr**) garantiza una conversión correcta. En el código siguiente se muestra un ejemplo en el que **SendMessage** devuelve un identificador a un pincel:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



A veces, el parámetro **CreateWindow** y **CreateWindowEx** *HMENU* se usa para pasar un identificador de control de tipo entero (ID). En este caso, debe convertir el identificador en un tipo **HMENU** :


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>Consideraciones adicionales

Para sacar el máximo partido de la comprobación **estricta** de tipos, debe seguir instrucciones adicionales. El código será más portátil en versiones futuras de Windows si realiza los siguientes cambios.

Los tipos **wParam**, **lParam**, **LRESULT** y **LPVOID** son *tipos de datos polimórficos*. Contienen distintos tipos de datos en momentos diferentes, incluso cuando está habilitada la comprobación **estricta** de tipos. Para aprovechar las ventajas de la comprobación de tipos, debe convertir los valores de estos tipos lo antes posible. (Tenga en cuenta que los atacantes de mensajes reconvierten *wParam* y *lParam* automáticamente de forma portátil).

Tenga especial cuidado para distinguir entre los tipos de **HMODULE** y **hInstance** . Incluso con **STRICT** Enabled, se definen como el mismo tipo base. La mayoría de las funciones de administración de módulos de kernel usan tipos **hInstance** , pero hay algunas funciones que devuelven o aceptan solo tipos **HMODULE** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Deshabilitar STRICT](disabling-strict.md)
</dt> <dt>

[Habilitar STRICT](enabling-strict.md)
</dt> </dl>

 

 