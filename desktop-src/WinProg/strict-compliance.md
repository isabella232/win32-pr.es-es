---
title: Cumplimiento strict
description: Es posible que algún código fuente que se compile correctamente produzca mensajes de error al habilitar la comprobación de tipos STRICT.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361709"
---
# <a name="strict-compliance"></a>Cumplimiento strict

Es posible que algún código fuente que se compile correctamente produzca mensajes de error al habilitar la comprobación de tipos **STRICT.** En las secciones siguientes se describen los requisitos mínimos para compilar el código **cuando strict** está habilitado. Se recomiendan pasos adicionales, especialmente para generar código portátil.

## <a name="general-requirements"></a>Requisitos generales

El requisito principal es que debe declarar tipos de identificador y punteros de función correctos en lugar de depender de tipos más generales. No se puede usar un tipo de identificador donde se espera otro. Esto también significa que es posible que tenga que cambiar las declaraciones de función y usar más conversión de tipos.

Para obtener mejores resultados, el tipo **HANDLE** genérico solo se debe usar cuando sea necesario.

## <a name="declaring-functions-within-your-application"></a>Declarar funciones dentro de la aplicación

Asegúrese de que se declaran todas las funciones de aplicación. Se recomienda colocar todas las declaraciones de función en un archivo include, ya que puede examinar fácilmente las declaraciones y buscar los tipos de parámetro y de valor devuelto que se deben cambiar.

Si usa la opción del compilador **/Zg** para crear archivos de encabezado para las funciones, recuerde que se obtienen resultados diferentes en función de si ha habilitado la comprobación de tipos **STRICT.** Con **STRICT** deshabilitado, todos los tipos de identificador generan el mismo tipo base. Con **STRICT** habilitado, generan tipos base diferentes. Para evitar conflictos, debe volver a crear el archivo de encabezado cada vez que habilite o deshabilite **STRICT,** o edite el archivo de encabezado para usar los tipos **HWND**, **HDC,** **HANDLE,** y así sucesivamente, en lugar de los tipos base.

Las declaraciones de función que copió de Windows.h en el código fuente pueden haber cambiado y es posible que la declaración local no esté actualizada. Quite la declaración local.

## <a name="types-that-require-casts"></a>Tipos que requieren casts

Algunas funciones tienen parámetros o tipos de valor devuelto genéricos. Por ejemplo, la [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) devuelve datos que pueden ser cualquier número de tipos, dependiendo del contexto. Cuando vea cualquiera de estas funciones en el código fuente, asegúrese de usar la conversión de tipos correcta y de que sea lo más específica posible. La lista siguiente es un ejemplo de estas funciones.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Al llamar a [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), primero debe convertir el resultado al tipo **UINT \_ PTR**. Debe realizar pasos similares para cualquier función que devuelva un **valor LRESULT** o **LONG \_ PTR,** donde el resultado contiene un identificador. Esto es necesario para escribir código portátil porque el tamaño de un identificador varía, dependiendo de la versión de Windows. La conversión (**UINT \_ PTR**) garantiza la conversión correcta. El código siguiente muestra un ejemplo en el que **SendMessage** devuelve un identificador a un pincel:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



El parámetro *hmenu* **CreateWindow** y **CreateWindowEx** se usa a veces para pasar un identificador de control entero (ID). En este caso, debe convertir el identificador a un **tipo HMENU:**


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

Para sacar el máximo partido de la comprobación de tipos **STRICT,** hay instrucciones adicionales que debe seguir. El código será más portátil en futuras versiones de Windows si realiza los cambios siguientes.

Los tipos **WPARAM,** **LPARAM,** **LRESULT** y **LPVOID** son *tipos de datos polimórficos.* Contiene diferentes tipos de datos en momentos diferentes, incluso cuando está habilitada la comprobación de tipos **STRICT.** Para obtener la ventaja de la comprobación de tipos, debe convertir los valores de estos tipos lo antes posible. (Tenga en cuenta que los generadores de mensajes se convierten automáticamente *en wParam* *y lParam* de forma portátil).

Debe tener especial cuidado para distinguir los **tipos HMODULE** **e HINSTANCE.** Incluso con **STRICT** habilitado, se definen como el mismo tipo base. La mayoría de las funciones de administración de módulos de kernel usan tipos **HINSTANCE,** pero hay algunas funciones que devuelven o aceptan solo **tipos HMODULE.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Deshabilitar STRICT](disabling-strict.md)
</dt> <dt>

[Habilitación de STRICT](enabling-strict.md)
</dt> </dl>

 

 