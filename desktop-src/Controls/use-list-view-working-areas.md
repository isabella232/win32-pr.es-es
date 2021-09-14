---
title: Uso de áreas List-View trabajo
description: En este tema se muestra cómo trabajar con áreas de trabajo de vista de lista. Las áreas de trabajo son áreas virtuales rectangulares que se pueden usar para organizar elementos en un control list-vew.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165417"
---
# <a name="how-to-use-list-view-working-areas"></a>Uso de áreas List-View trabajo

En este tema se muestra cómo trabajar con áreas de trabajo de vista de lista. Las áreas de trabajo son áreas virtuales rectangulares que se pueden usar para organizar elementos en un control list-vew. Un área de trabajo no es una ventana y no puede tener un borde visible. De forma predeterminada, el control list-view no tiene áreas de trabajo. Al crear un área de trabajo, puede crear un borde vacío en la parte izquierda, superior o derecha de los elementos o hacer que se muestre una barra de desplazamiento horizontal cuando normalmente no hubiera uno.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-working-area"></a>Creación de un área de trabajo

En el siguiente ejemplo de código de C++ se muestra cómo crear un área de trabajo con un borde vacío de 25 píxeles en sus lados superior, izquierdo y derecho.


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a>Creación de varias áreas de trabajo

En el siguiente ejemplo de código de C++ se muestra cómo crear dos áreas de trabajo en un control . Cada área de trabajo usa aproximadamente la mitad del área de cliente y está rodeado por un borde vacío de 25 píxeles.


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Determinar el área de trabajo a la que pertenece un elemento

Una manera de determinar a qué área de trabajo pertenece un elemento es hacer lo siguiente:

-   Recupere la lista de coordenadas de todas las áreas de trabajo del control list-view.
-   Recupere las coordenadas del elemento.
-   Determine si las coordenadas del elemento se encuentran dentro de las coordenadas de una de las áreas de trabajo.

La función definida por la aplicación en el siguiente ejemplo de código de C++ devuelve el índice del área de trabajo a la que pertenece el elemento. Si se produce un error en la función, devuelve –1. Si la función se realiza correctamente, pero el elemento no está dentro de ninguna de las áreas de trabajo, la función devuelve 0, porque todos los elementos que no están dentro de un área de trabajo se convierten automáticamente en miembros del área de trabajo cero.


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 




