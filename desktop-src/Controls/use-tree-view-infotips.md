---
title: Cómo usar Tree-View recuadros informativos
description: Cuando se aplica el estilo de recuadro de TV \_ a un control de vista de árbol, genera \_ notificaciones de TVN GETINFOTIP cuando el cursor está sobre un elemento de la vista de árbol. Al responder a esta notificación, puede establecer el texto que aparece en el recuadro informativo.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105656311"
---
# <a name="how-to-use-tree-view-infotips"></a>Cómo usar Tree-View recuadros informativos

Cuando se aplica el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) a un control de vista de árbol, genera notificaciones de [TVN \_ GETINFOTIP](tvn-getinfotip.md) cuando el cursor está sobre un elemento de la vista de árbol. Al responder a esta notificación, puede establecer el texto que aparece en el recuadro informativo.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-tree-view-infotips"></a>Usar Tree-View recuadros informativos

En el ejemplo de código siguiente se muestra cómo una aplicación puede responder a la notificación. Para simplificar, el ejemplo solo copia el texto del elemento en el recuadro informativo.


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Tree-View](using-treeview.md)
</dt> <dt>

[En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




