---
title: Cómo trabajar con índices de imagen de estado
description: A menudo hay confusión sobre cómo establecer y recuperar el índice de imagen de estado en un control de vista de árbol.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165170"
---
# <a name="how-to-work-with-state-image-indexes"></a>Cómo trabajar con índices de imagen de estado

A menudo hay confusión sobre cómo establecer y recuperar el índice de imagen de estado en un control de vista de árbol. En los ejemplos siguientes se muestra el método adecuado para establecer y recuperar el índice de imagen de estado. En los ejemplos se supone que solo hay dos índices de imagen de estado en el control de vista de árbol, desactivados y activados. Si la aplicación contiene más de dos, estas funciones tendrán que modificarse para controlar ese caso.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="set-a-tree-view-items-check-state"></a>Establecer el Tree-View de comprobación de un elemento de seguridad

En el ejemplo siguiente se muestra cómo establecer el estado de comprobación de un elemento de vista de árbol.


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperación del Tree-View de comprobación de un elemento

En el ejemplo siguiente se muestra cómo recuperar el estado de comprobación de un elemento de vista de árbol.


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Tree-View controles](using-treeview.md)
</dt> <dt>

[El ejemplo CustDTv muestra el dibujo personalizado en un control Tree-View datos](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




