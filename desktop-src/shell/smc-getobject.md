---
description: Solicita un puntero a un objeto especificado.
title: Mensaje de SMC_GETOBJECT (shobjidl. h)
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
ms.openlocfilehash: 5d0c0592356bff13e60c122b3c88cad05733e4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997789"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="55044-103">\_Mensaje GETOBJECT de SMC</span><span class="sxs-lookup"><span data-stu-id="55044-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="55044-104">Solicita un puntero a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="55044-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="55044-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55044-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55044-106">*suscripto*</span><span class="sxs-lookup"><span data-stu-id="55044-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="55044-107">IID asociado al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="55044-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="55044-108">*FV*</span><span class="sxs-lookup"><span data-stu-id="55044-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="55044-109">Puntero void que recibe un puntero a la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="55044-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55044-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55044-110">Return value</span></span>

<span data-ttu-id="55044-111">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="55044-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="55044-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55044-112">Remarks</span></span>

<span data-ttu-id="55044-113">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="55044-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="55044-114">Cree el objeto solicitado y asigne un puntero a la interfaz solicitada a *PV*.</span><span class="sxs-lookup"><span data-stu-id="55044-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="55044-115">Se pueden solicitar las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="55044-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="55044-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="55044-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="55044-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="55044-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="55044-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="55044-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="55044-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="55044-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="55044-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55044-120">Requirements</span></span>



| <span data-ttu-id="55044-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="55044-121">Requirement</span></span> | <span data-ttu-id="55044-122">Value</span><span class="sxs-lookup"><span data-stu-id="55044-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55044-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55044-123">Minimum supported client</span></span><br/> | <span data-ttu-id="55044-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55044-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55044-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55044-125">Minimum supported server</span></span><br/> | <span data-ttu-id="55044-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55044-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55044-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55044-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="55044-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55044-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="55044-129">IDL</span><span class="sxs-lookup"><span data-stu-id="55044-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55044-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55044-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
