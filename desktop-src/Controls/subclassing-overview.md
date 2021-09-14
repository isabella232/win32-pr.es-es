---
title: Controles de subclases
description: Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclases.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166970"
---
# <a name="subclassing-controls"></a>Controles de subclases

Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclases. Una subclase puede tener todas las características de una clase existente, así como las características adicionales que quiera proporcionar.

En este documento se describe cómo se crean las subclases e incluye los temas siguientes.

-   [Controles de subclases anteriores a ComCtl32.dll versión 6](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [Almacenamiento de datos de usuario](#storing-user-data)
    -   [Desventajas del enfoque de subclases antiguo](#disadvantages-of-the-old-subclassing-approach)
-   [Controles de subclases mediante ComCtl32.dll versión 6](#subclassing-controls-using-comctl32dll-version-6)
    -   [SetWindowSubclass](#setwindowsubclass)
    -   [GetWindowSubclass](#getwindowsubclass)
    -   [RemoveWindowSubclass](#removewindowsubclass)
    -   [DefSubclassProc](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a>Controles de subclases anteriores a ComCtl32.dll versión 6

Puede colocar un control en una subclase y almacenar datos de usuario dentro de un control . Esto se hace cuando se usan versiones de ComCtl32.dll anteriores a la versión 6. Hay algunas desventajas en la creación de subclases con versiones anteriores de ComCtl32.dll.

Para crear un nuevo control, es mejor empezar con uno de los Windows comunes y ampliarlo para adaptarlo a una necesidad determinada. Para extender un control, cree un control y reemplace su procedimiento de ventana existente por uno nuevo. El nuevo procedimiento intercepta los mensajes del control y actúa sobre ellos o los pasa al procedimiento original para el procesamiento predeterminado. Use las [**funciones SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) [**o SetWindowLongPtr para**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) reemplazar el WNDPROC del control. En el ejemplo de código siguiente se muestra cómo reemplazar un WNDPROC.


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a>Almacenamiento de datos de usuario

Es posible que desee almacenar datos de usuario con una ventana individual. El nuevo procedimiento de ventana puede usar estos datos para determinar cómo dibujar el control o dónde enviar determinados mensajes. Por ejemplo, puede usar datos para almacenar un puntero de clase de C++ a la clase que representa el control. En el ejemplo de código siguiente se muestra cómo usar [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) para almacenar datos con una ventana.


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a>Desventajas del enfoque de subclases antiguo

En la lista siguiente se apuntan algunas de las desventajas de usar el enfoque descrito anteriormente para crear subclases de un control.

-   El procedimiento de ventana solo se puede reemplazar una vez.
-   Es difícil quitar una subclase después de crearla.
-   La asociación de datos privados a una ventana es ineficaz.
-   Para llamar al siguiente procedimiento en una cadena de subclase, no puede convertir el procedimiento de ventana anterior y llamarlo, debe llamarlo mediante la [**función CallWindowProc.**](/windows/desktop/api/winuser/nf-winuser-callwindowproca)

## <a name="subclassing-controls-using-comctl32dll-version-6"></a>Controles de subclases mediante ComCtl32.dll versión 6

> [!Note]  
> ComCtl32.dll versión 6 es solo Unicode. Los controles comunes admitidos por ComCtl32.dll versión 6 no deben ser subclases (o superclases) con procedimientos de ventana ANSI.

 

ComCtl32.dll versión 6 contiene cuatro funciones que facilitan la creación de subclases y eliminan las desventajas que se han analizado anteriormente. Las nuevas funciones encapsulan la administración implicada con varios conjuntos de datos de referencia, por lo que el desarrollador puede centrarse en las características de programación y no en la administración de subclases. Las funciones de subclases son:

-   [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a>SetWindowSubclass

Esta función se usa para crear inicialmente una subclase de una ventana. Cada subclase se identifica de forma única mediante la dirección de *pfnSubclass* y *su uIdSubclass*. Ambos son parámetros de la [**función SetWindowSubclass.**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) Varias subclases pueden compartir el mismo procedimiento de subclase y el identificador puede identificar cada llamada. Para cambiar los datos de referencia, puede realizar llamadas posteriores **a SetWindowSubclass**. La ventaja importante es que cada instancia de subclase tiene sus propios datos de referencia.

La declaración de un procedimiento de subclase es ligeramente diferente de un procedimiento de ventana normal porque tiene dos fragmentos de datos adicionales: el identificador de subclase y los datos de referencia. Los dos últimos parámetros de la siguiente declaración de función lo muestran.


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



Cada vez que el nuevo procedimiento de ventana recibe un mensaje, se incluyen un identificador de subclase y datos de referencia.

> [!Note]  
> Todas las cadenas que se pasan al procedimiento son cadenas Unicode incluso si Unicode no se especifica como definición de preprocesador.

 

En el ejemplo siguiente se muestra una implementación de esqueleto de un procedimiento de ventana para un control con subclases.


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



El procedimiento de ventana se puede adjuntar al control en el controlador [**\_ WM INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) del procedimiento de diálogo, como se muestra en el ejemplo siguiente.


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a>GetWindowSubclass

Esta función recupera información sobre una subclase. Por ejemplo, puede usar [**GetWindowSubclass para**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) acceder a los datos de referencia.

### <a name="removewindowsubclass"></a>RemoveWindowSubclass

Esta función quita las subclases. [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) en combinación [**con SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) permite agregar y quitar subclases dinámicamente.

### <a name="defsubclassproc"></a>DefSubclassProc

La [**función DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) llama al siguiente controlador de la cadena de subclase. La función también recupera el identificador y los datos de referencia adecuados y pasa la información al siguiente procedimiento de ventana.

 

 