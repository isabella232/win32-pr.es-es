---
description: 'SMC_GETSFOBJECT mensaje: solicita un puntero a un objeto especificado.'
title: SMC_GETSFOBJECT mensaje (Shobjidl.h)
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
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086613"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="c0621-103">Mensaje \_ DE SMC GETSFOBJECT</span><span class="sxs-lookup"><span data-stu-id="c0621-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="c0621-104">Solicita un puntero a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c0621-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="c0621-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0621-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0621-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="c0621-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="c0621-107">El IID asociado al objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="c0621-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="c0621-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="c0621-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="c0621-109">Puntero void que recibe un puntero a la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="c0621-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0621-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0621-110">Return value</span></span>

<span data-ttu-id="c0621-111">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0621-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0621-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0621-112">Remarks</span></span>

<span data-ttu-id="c0621-113">El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c0621-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="c0621-114">Es similar a [**SMC \_ GETOBJECT, pero**](smc-getobject.md) se usa para los elementos de carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="c0621-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="c0621-115">Cree el objeto solicitado y asigne un puntero a la interfaz solicitada a *pv*.</span><span class="sxs-lookup"><span data-stu-id="c0621-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="c0621-116">Se pueden solicitar las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="c0621-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="c0621-117">**Istream**</span><span class="sxs-lookup"><span data-stu-id="c0621-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="c0621-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="c0621-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="c0621-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="c0621-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="c0621-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0621-120">Requirements</span></span>



| <span data-ttu-id="c0621-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0621-121">Requirement</span></span> | <span data-ttu-id="c0621-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c0621-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0621-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0621-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0621-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c0621-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0621-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0621-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0621-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0621-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0621-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0621-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0621-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0621-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0621-129">Idl</span><span class="sxs-lookup"><span data-stu-id="c0621-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0621-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0621-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
