---
description: 'SMC_GETOBJECT mensaje: solicita un puntero a un objeto especificado.'
title: SMC_GETOBJECT mensaje (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100443"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="47fd4-103">Mensaje \_ GETOBJECT de SMC</span><span class="sxs-lookup"><span data-stu-id="47fd4-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="47fd4-104">Solicita un puntero a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="47fd4-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="47fd4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47fd4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47fd4-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="47fd4-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="47fd4-107">El IID asociado al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="47fd4-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="47fd4-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="47fd4-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="47fd4-109">Puntero void que recibe un puntero a la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="47fd4-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47fd4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47fd4-110">Return value</span></span>

<span data-ttu-id="47fd4-111">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47fd4-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="47fd4-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47fd4-112">Remarks</span></span>

<span data-ttu-id="47fd4-113">El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="47fd4-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="47fd4-114">Cree el objeto solicitado y asigne un puntero a la interfaz solicitada a *pv*.</span><span class="sxs-lookup"><span data-stu-id="47fd4-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="47fd4-115">Se pueden solicitar las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="47fd4-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="47fd4-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="47fd4-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="47fd4-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="47fd4-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="47fd4-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="47fd4-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="47fd4-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="47fd4-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="47fd4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47fd4-120">Requirements</span></span>



| <span data-ttu-id="47fd4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47fd4-121">Requirement</span></span> | <span data-ttu-id="47fd4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47fd4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47fd4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47fd4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47fd4-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="47fd4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47fd4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47fd4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47fd4-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47fd4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47fd4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47fd4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="47fd4-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="47fd4-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="47fd4-129">Idl</span><span class="sxs-lookup"><span data-stu-id="47fd4-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47fd4-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="47fd4-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
