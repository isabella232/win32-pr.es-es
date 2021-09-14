---
title: Cómo usar información Tree-View datos
description: Al aplicar el estilo INFOTIP de TVS a un control de vista de árbol, genera notificaciones GETINFOTIP de TVN cuando el cursor está sobre un elemento de la vista \_ \_ de árbol. Al responder a esta notificación, puede establecer el texto que aparece en la información.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165377"
---
# <a name="how-to-use-tree-view-infotips"></a>Cómo usar información Tree-View datos

Al aplicar el estilo [**\_ INFOTIP**](tree-view-control-window-styles.md) de TVS a un control de vista de árbol, genera notificaciones [ \_ GETINFOTIP](tvn-getinfotip.md) de TVN cuando el cursor está sobre un elemento de la vista de árbol. Al responder a esta notificación, puede establecer el texto que aparece en la información.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-tree-view-infotips"></a>Uso de Tree-View información general

El código de ejemplo siguiente muestra cómo una aplicación podría responder a la notificación. Por motivos de simplicidad, el ejemplo simplemente copia el texto del elemento en la información.


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

[Usar Tree-View controles](using-treeview.md)
</dt> <dt>

[El ejemplo CustDTv muestra el dibujo personalizado en un control Tree-View datos](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




