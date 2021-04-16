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
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="313a6-104">Cómo usar Tree-View recuadros informativos</span><span class="sxs-lookup"><span data-stu-id="313a6-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="313a6-105">Cuando se aplica el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) a un control de vista de árbol, genera notificaciones de [TVN \_ GETINFOTIP](tvn-getinfotip.md) cuando el cursor está sobre un elemento de la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="313a6-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="313a6-106">Al responder a esta notificación, puede establecer el texto que aparece en el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="313a6-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="313a6-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="313a6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="313a6-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="313a6-108">Technologies</span></span>

-   [<span data-ttu-id="313a6-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="313a6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="313a6-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="313a6-110">Prerequisites</span></span>

-   <span data-ttu-id="313a6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="313a6-111">C/C++</span></span>
-   <span data-ttu-id="313a6-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="313a6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="313a6-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="313a6-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="313a6-114">Usar Tree-View recuadros informativos</span><span class="sxs-lookup"><span data-stu-id="313a6-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="313a6-115">En el ejemplo de código siguiente se muestra cómo una aplicación puede responder a la notificación.</span><span class="sxs-lookup"><span data-stu-id="313a6-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="313a6-116">Para simplificar, el ejemplo solo copia el texto del elemento en el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="313a6-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="313a6-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="313a6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="313a6-118">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="313a6-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="313a6-119">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="313a6-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




