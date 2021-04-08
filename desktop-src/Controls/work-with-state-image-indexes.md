---
title: Cómo trabajar con índices de imagen de estado
description: A menudo hay confusión sobre cómo establecer y recuperar el índice de la imagen de estado en un control de vista de árbol.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788902"
---
# <a name="how-to-work-with-state-image-indexes"></a>Cómo trabajar con índices de imagen de estado

A menudo hay confusión sobre cómo establecer y recuperar el índice de la imagen de estado en un control de vista de árbol. En los siguientes ejemplos se muestra el método adecuado para establecer y recuperar el índice de la imagen de estado. En los ejemplos se da por hecho que solo hay dos índices de imagen de estado en el control de vista de árbol, desactivados y comprobados. Si la aplicación contiene más de dos, estas funciones deberán modificarse para controlar ese caso.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="set-a-tree-view-items-check-state"></a>Establecer el estado de comprobación de un elemento de Tree-View

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



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperar el estado de comprobación de un elemento de Tree-View

En el ejemplo siguiente se muestra cómo recuperar el estado de comprobación de un elemento de la vista de árbol.


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

[Usar controles Tree-View](using-treeview.md)
</dt> <dt>

[En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




