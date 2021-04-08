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
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="f9466-103">Cómo trabajar con índices de imagen de estado</span><span class="sxs-lookup"><span data-stu-id="f9466-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="f9466-104">A menudo hay confusión sobre cómo establecer y recuperar el índice de la imagen de estado en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f9466-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="f9466-105">En los siguientes ejemplos se muestra el método adecuado para establecer y recuperar el índice de la imagen de estado.</span><span class="sxs-lookup"><span data-stu-id="f9466-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="f9466-106">En los ejemplos se da por hecho que solo hay dos índices de imagen de estado en el control de vista de árbol, desactivados y comprobados.</span><span class="sxs-lookup"><span data-stu-id="f9466-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="f9466-107">Si la aplicación contiene más de dos, estas funciones deberán modificarse para controlar ese caso.</span><span class="sxs-lookup"><span data-stu-id="f9466-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f9466-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="f9466-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f9466-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="f9466-109">Technologies</span></span>

-   [<span data-ttu-id="f9466-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="f9466-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f9466-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9466-111">Prerequisites</span></span>

-   <span data-ttu-id="f9466-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="f9466-112">C/C++</span></span>
-   <span data-ttu-id="f9466-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="f9466-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f9466-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f9466-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="f9466-115">Establecer el estado de comprobación de un elemento de Tree-View</span><span class="sxs-lookup"><span data-stu-id="f9466-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="f9466-116">En el ejemplo siguiente se muestra cómo establecer el estado de comprobación de un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f9466-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


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



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="f9466-117">Recuperar el estado de comprobación de un elemento de Tree-View</span><span class="sxs-lookup"><span data-stu-id="f9466-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="f9466-118">En el ejemplo siguiente se muestra cómo recuperar el estado de comprobación de un elemento de la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="f9466-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f9466-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9466-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9466-120">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="f9466-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="f9466-121">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="f9466-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




