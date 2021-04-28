---
description: 'DFM_WM_INITMENUPOPUP mensaje: se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.'
title: DFM_WM_INITMENUPOPUP mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097003"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="03dfc-104">Mensaje \_ INITMENUPOPUP de DFM WM \_</span><span class="sxs-lookup"><span data-stu-id="03dfc-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="03dfc-105">Se envía cuando un menú desplegable o submenú está a punto de activarse.</span><span class="sxs-lookup"><span data-stu-id="03dfc-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="03dfc-106">Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.</span><span class="sxs-lookup"><span data-stu-id="03dfc-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="03dfc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03dfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03dfc-108">*wParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="03dfc-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03dfc-109">Identificador del menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="03dfc-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="03dfc-110">*lParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="03dfc-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03dfc-111">La palabra de orden bajo especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="03dfc-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="03dfc-112">La palabra de orden superior indica si el menú desplegable es el menú de la ventana.</span><span class="sxs-lookup"><span data-stu-id="03dfc-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="03dfc-113">Si el menú es el menú de la ventana, este parámetro es **TRUE**; de lo contrario, es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="03dfc-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03dfc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03dfc-114">Return value</span></span>

<span data-ttu-id="03dfc-115">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="03dfc-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="03dfc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03dfc-116">Requirements</span></span>



| <span data-ttu-id="03dfc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="03dfc-117">Requirement</span></span> | <span data-ttu-id="03dfc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="03dfc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03dfc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03dfc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="03dfc-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="03dfc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="03dfc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03dfc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="03dfc-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="03dfc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03dfc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03dfc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="03dfc-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="03dfc-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




