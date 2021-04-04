---
title: Cómo usar áreas de trabajo de List-View
description: En este tema se muestra cómo trabajar con áreas de trabajo de la vista de lista. Las áreas de trabajo son áreas virtuales rectangulares que se pueden utilizar para organizar los elementos en un control List-vista.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075554"
---
# <a name="how-to-use-list-view-working-areas"></a>Cómo usar áreas de trabajo de List-View

En este tema se muestra cómo trabajar con áreas de trabajo de la vista de lista. Las áreas de trabajo son áreas virtuales rectangulares que se pueden utilizar para organizar los elementos en un control List-vista. Un área de trabajo no es una ventana y no puede tener un borde visible. De forma predeterminada, el control de vista de lista no tiene áreas de trabajo. Al crear un área de trabajo, puede crear un borde vacío en la parte izquierda, superior o derecha de los elementos, o hacer que se muestre una barra de desplazamiento horizontal cuando normalmente no hubiera ninguno.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="create-a-working-area"></a>Crear un área de trabajo

En el ejemplo de código de C++ siguiente se muestra cómo crear un área de trabajo con un borde vacío de 25 píxeles en los lados superior, izquierdo y derecho.


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



### <a name="create-multiple-working-areas"></a>Crear varias áreas de trabajo

En el ejemplo de código de C++ siguiente se muestra cómo crear dos áreas de trabajo en un control. Cada área de trabajo utiliza aproximadamente la mitad del área cliente y está rodeada por un borde vacío de 25 píxeles.


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

Una manera de determinar el área de trabajo a la que pertenece un elemento es hacer lo siguiente:

-   Recupere la lista de coordenadas de todas las áreas de trabajo en el control de vista de lista.
-   Recupera las coordenadas del elemento.
-   Determine si las coordenadas del elemento se encuentran dentro de las coordenadas de una de las áreas de trabajo.

La función definida por la aplicación en el siguiente ejemplo de código de C++ devuelve el índice del área de trabajo al que pertenece el elemento. Si se produce un error en la función, devuelve – 1. Si la función se ejecuta correctamente, pero el elemento no está dentro de ninguna de las áreas de trabajo, la función devuelve 0, porque todos los elementos que no están dentro de un área de trabajo se convierten automáticamente en un miembro del área de trabajo cero.


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

[Referencia de control de vista de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




