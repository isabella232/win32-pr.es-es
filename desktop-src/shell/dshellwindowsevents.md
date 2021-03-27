---
description: Recibe los eventos de registro de la ventana IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987552"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="6c32d-103">Objeto DShellWindowsEvents</span><span class="sxs-lookup"><span data-stu-id="6c32d-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="6c32d-104">Recibe los eventos de registro de la ventana [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .</span><span class="sxs-lookup"><span data-stu-id="6c32d-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="6c32d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c32d-105">Members</span></span>

<span data-ttu-id="6c32d-106">El objeto **DShellWindowsEvents** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c32d-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="6c32d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c32d-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c32d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c32d-108">Methods</span></span>

<span data-ttu-id="6c32d-109">El objeto **DShellWindowsEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6c32d-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="6c32d-110">Método</span><span class="sxs-lookup"><span data-stu-id="6c32d-110">Method</span></span>                                                           | <span data-ttu-id="6c32d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c32d-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="6c32d-112">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="6c32d-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="6c32d-113">Se llama cuando una ventana se registra como una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="6c32d-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="6c32d-114">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="6c32d-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="6c32d-115">Se llama cuando se revoca el registro de una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="6c32d-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c32d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c32d-116">Remarks</span></span>

<span data-ttu-id="6c32d-117">Use **DShellWindowsEvents** para supervisar Cuándo se registra o revoca una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="6c32d-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="6c32d-118">Para obtener más información, vea [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="6c32d-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c32d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c32d-119">Requirements</span></span>



| <span data-ttu-id="6c32d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c32d-120">Requirement</span></span> | <span data-ttu-id="6c32d-121">Value</span><span class="sxs-lookup"><span data-stu-id="6c32d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c32d-122">Producto</span><span class="sxs-lookup"><span data-stu-id="6c32d-122">Product</span></span><br/> | <span data-ttu-id="6c32d-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="6c32d-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="6c32d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c32d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6c32d-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c32d-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="6c32d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c32d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c32d-127"><dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6c32d-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="6c32d-128">IID</span><span class="sxs-lookup"><span data-stu-id="6c32d-128">IID</span></span><br/>     | <span data-ttu-id="6c32d-129">\_ISHELLWINDOWS IID</span><span class="sxs-lookup"><span data-stu-id="6c32d-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6c32d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c32d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c32d-131">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="6c32d-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




