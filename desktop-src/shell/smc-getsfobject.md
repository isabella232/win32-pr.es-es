---
description: Solicita un puntero a un objeto especificado.
title: Mensaje de SMC_GETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277632"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="b9713-103">Mensaje de GETSFOBJECT de SMC \_</span><span class="sxs-lookup"><span data-stu-id="b9713-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="b9713-104">Solicita un puntero a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b9713-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="b9713-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9713-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9713-106">*suscripto*</span><span class="sxs-lookup"><span data-stu-id="b9713-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="b9713-107">IID asociado al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="b9713-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="b9713-108">*FV*</span><span class="sxs-lookup"><span data-stu-id="b9713-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="b9713-109">Puntero void que recibe un puntero a la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="b9713-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9713-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9713-110">Return value</span></span>

<span data-ttu-id="b9713-111">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b9713-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9713-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9713-112">Remarks</span></span>

<span data-ttu-id="b9713-113">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b9713-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="b9713-114">Es similar a [**SMC \_ GETOBJECT**](smc-getobject.md) pero se usa para los elementos de carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="b9713-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="b9713-115">Cree el objeto solicitado y asigne un puntero a la interfaz solicitada a *PV*.</span><span class="sxs-lookup"><span data-stu-id="b9713-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="b9713-116">Se pueden solicitar las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="b9713-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="b9713-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="b9713-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="b9713-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="b9713-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="b9713-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="b9713-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="b9713-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9713-120">Requirements</span></span>



| <span data-ttu-id="b9713-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9713-121">Requirement</span></span> | <span data-ttu-id="b9713-122">Value</span><span class="sxs-lookup"><span data-stu-id="b9713-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9713-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9713-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9713-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b9713-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9713-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9713-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9713-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9713-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9713-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9713-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9713-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9713-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9713-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b9713-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9713-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9713-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
