---
title: Subclase de controles
description: Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclase.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078468"
---
# <a name="subclassing-controls"></a>Subclase de controles

Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclase. Una subclase puede tener todas las características de una clase existente, así como las características adicionales que desee proporcionar.

En este documento se explica cómo se crean las subclases e incluye los temas siguientes.

-   [Subclase de controles anteriores a ComCtl32.dll versión 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Almacenar datos de usuario](#storing-user-data)
    -   [Desventajas del enfoque de subclases anterior](#disadvantages-of-the-old-subclassing-approach)
-   [Subclase de controles con ComCtl32.dll versión 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Subclase de controles anteriores a ComCtl32.dll versión 6

Puede colocar un control en una subclase y almacenar los datos de usuario dentro de un control. Esto se hace al usar versiones de ComCtl32.dll anteriores a la versión 6. La creación de subclases con versiones anteriores de ComCtl32.dll tiene algunas desventajas.

Para crear un nuevo control, es mejor empezar con uno de los controles comunes de Windows y extenderlo para que se ajuste a una necesidad concreta. Para extender un control, cree un control y reemplace su procedimiento de ventana existente por uno nuevo. El nuevo procedimiento intercepta los mensajes del control y actúa en ellos o los pasa al procedimiento original para el procesamiento predeterminado. Utilice la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) para reemplazar el WndProc del control. En el ejemplo de código siguiente se muestra cómo reemplazar un WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Almacenar datos de usuario

Es posible que desee almacenar los datos de usuario con una ventana individual. El nuevo procedimiento de ventana puede usar estos datos para determinar cómo dibujar el control o dónde enviar determinados mensajes. Por ejemplo, puede usar los datos para almacenar un puntero de clase de C++ en la clase que representa el control. En el ejemplo de código siguiente se muestra cómo usar [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) para almacenar datos con una ventana.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Desventajas del enfoque de subclases anterior

En la lista siguiente se indican algunas de las desventajas del uso del enfoque descrito anteriormente para subclases de un control.

-   El procedimiento de ventana solo se puede reemplazar una vez.
-   Es difícil quitar una subclase una vez creada.
-   La Asociación de datos privados con una ventana es ineficaz.
-   Para llamar al siguiente procedimiento en una cadena de subclases, no puede convertir el procedimiento de ventana anterior y llamarlo; debe llamarlo mediante la función [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Subclase de controles con ComCtl32.dll versión 6

> [!Note]  
> ComCtl32.dll versión 6 solo es Unicode. Los controles comunes admitidos por ComCtl32.dll versión 6 no deben ser subclases (o superclase) con procedimientos de ventana ANSI.

 

ComCtl32.dll versión 6 contiene cuatro funciones que facilitan la creación de subclases y eliminan las desventajas descritas anteriormente. Las nuevas funciones encapsulan la administración implicada en varios conjuntos de datos de referencia, por lo que el desarrollador puede centrarse en las características de programación y no en la administración de subclases. Las funciones de subclase son:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Esta función se usa para subclaser inicialmente una ventana. Cada subclase se identifica de forma única mediante la dirección de *pfnSubclass* y su *uIdSubclass*. Ambos son parámetros de la función [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) . Varias subclases pueden compartir el mismo procedimiento de subclase y el identificador puede identificar cada llamada. Para cambiar los datos de referencia, puede realizar llamadas subsiguientes a **SetWindowSubclass**. La ventaja importante es que cada instancia de la subclase tiene sus propios datos de referencia.

La declaración de un procedimiento de subclase es ligeramente diferente de un procedimiento de ventana normal porque tiene dos elementos de datos adicionales: el identificador de la subclase y los datos de referencia. Los dos últimos parámetros de la declaración de función siguiente muestran esto.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Cada vez que el nuevo procedimiento de ventana recibe un mensaje, se incluyen un identificador de subclase y datos de referencia.

> [!Note]  
> Todas las cadenas que se pasan al procedimiento son cadenas Unicode incluso si no se especifica Unicode como definición del preprocesador.

 

En el ejemplo siguiente se muestra una implementación esqueleto de un procedimiento de ventana para un control de subclase.


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



El procedimiento de ventana se puede adjuntar al control en el controlador [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) del procedimiento del cuadro de diálogo, como se muestra en el ejemplo siguiente.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Esta función recupera información sobre una subclase. Por ejemplo, puede usar [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) para tener acceso a los datos de referencia.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Esta función quita las subclases. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) en combinación con [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) permite agregar y quitar de forma dinámica las subclases.

### <a name="defsubclassproc"></a>DefSubclassProc

La función [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) llama al siguiente controlador de la cadena de subclases. La función también recupera el identificador y los datos de referencia apropiados y pasa la información al procedimiento de ventana siguiente.

 

 