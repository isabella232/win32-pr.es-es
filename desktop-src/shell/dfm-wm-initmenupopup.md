---
description: Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.
title: Mensaje de DFM_WM_INITMENUPOPUP (ShlObj. h)
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153913"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="11e64-104">DFM \_ WM \_ INITMENUPOPUP Message</span><span class="sxs-lookup"><span data-stu-id="11e64-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="11e64-105">Se envía cuando un menú desplegable o un submenú está a punto de activarse.</span><span class="sxs-lookup"><span data-stu-id="11e64-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="11e64-106">Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.</span><span class="sxs-lookup"><span data-stu-id="11e64-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="11e64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11e64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e64-108">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11e64-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e64-109">Identificador del menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="11e64-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="11e64-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11e64-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e64-111">La palabra de orden inferior especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="11e64-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="11e64-112">La palabra de orden superior indica si el menú desplegable es el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="11e64-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="11e64-113">Si el menú es el menú ventana, este parámetro es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="11e64-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e64-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11e64-114">Return value</span></span>

<span data-ttu-id="11e64-115">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="11e64-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e64-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11e64-116">Requirements</span></span>



| <span data-ttu-id="11e64-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e64-117">Requirement</span></span> | <span data-ttu-id="11e64-118">Value</span><span class="sxs-lookup"><span data-stu-id="11e64-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11e64-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e64-119">Minimum supported client</span></span><br/> | <span data-ttu-id="11e64-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11e64-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="11e64-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11e64-121">Minimum supported server</span></span><br/> | <span data-ttu-id="11e64-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11e64-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11e64-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11e64-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e64-124"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e64-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




