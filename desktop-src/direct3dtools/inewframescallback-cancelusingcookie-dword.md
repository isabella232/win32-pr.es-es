---
description: Devolución de llamada que notifica al host de una solicitud cancelada mediante una cookie que identifica de forma única la solicitud.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'INewFramesCallback:: CancelUsingCookie (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494716"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="1a0fc-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback:: CancelUsingCookie (método)</span><span class="sxs-lookup"><span data-stu-id="1a0fc-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="1a0fc-104">Devolución de llamada que notifica al host de una solicitud cancelada mediante una cookie que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a0fc-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a0fc-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="1a0fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a0fc-106">Parameters</span></span>

<span data-ttu-id="1a0fc-107">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1a0fc-107">*requestCookie* </span></span>  
<span data-ttu-id="1a0fc-108">La cookie que idenfies de forma única la solicitud cancelada.</span><span class="sxs-lookup"><span data-stu-id="1a0fc-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a0fc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a0fc-109">Return value</span></span>

<span data-ttu-id="1a0fc-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1a0fc-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a0fc-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a0fc-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0fc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a0fc-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a0fc-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a0fc-113">Header</span></span></p></td><td><span data-ttu-id="1a0fc-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1a0fc-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1a0fc-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="1a0fc-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1a0fc-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="1a0fc-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
