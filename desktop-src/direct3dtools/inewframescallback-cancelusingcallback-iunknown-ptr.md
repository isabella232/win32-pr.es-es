---
description: Devolución de llamada que notifica al host de una solicitud cancelada.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'INewFramesCallback:: CancelUsingCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495743"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="71dc3-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback:: CancelUsingCallback (método)</span><span class="sxs-lookup"><span data-stu-id="71dc3-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="71dc3-104">Devolución de llamada que notifica al host de una solicitud cancelada.</span><span class="sxs-lookup"><span data-stu-id="71dc3-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71dc3-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="71dc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71dc3-106">Parameters</span></span>

<span data-ttu-id="71dc3-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="71dc3-107">*requestCallback* </span></span>  
<span data-ttu-id="71dc3-108">Dirección de la solicitud cancelada.</span><span class="sxs-lookup"><span data-stu-id="71dc3-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="71dc3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71dc3-109">Return value</span></span>

<span data-ttu-id="71dc3-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="71dc3-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71dc3-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71dc3-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="71dc3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71dc3-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="71dc3-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71dc3-113">Header</span></span></p></td><td><span data-ttu-id="71dc3-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="71dc3-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="71dc3-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="71dc3-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="71dc3-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="71dc3-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
