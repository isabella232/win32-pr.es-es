---
description: Función de devolución de llamada que se usa para notificar al host los resultados de una acción (por ejemplo, capturar un fotograma) que solicitó.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunActionCallback:: objeto requestresult (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152617"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span data-ttu-id="b7eb0-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback:: objeto requestresult (método)</span><span class="sxs-lookup"><span data-stu-id="b7eb0-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback::RequestResult method</span></span>

<span data-ttu-id="b7eb0-104">Función de devolución de llamada que se usa para notificar al host los resultados de una acción (por ejemplo, capturar un fotograma) que solicitó.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-104">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7eb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7eb0-105">Syntax</span></span>


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a><span data-ttu-id="b7eb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7eb0-106">Parameters</span></span>

<span data-ttu-id="b7eb0-107">*actionResult* </span><span class="sxs-lookup"><span data-stu-id="b7eb0-107">*actionResult* </span></span>  
<span data-ttu-id="b7eb0-108">El resultado de la acción.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-108">The result of the action.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7eb0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7eb0-109">Return value</span></span>

<span data-ttu-id="b7eb0-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7eb0-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7eb0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7eb0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7eb0-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b7eb0-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7eb0-113">Header</span></span></p></td><td><span data-ttu-id="b7eb0-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b7eb0-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b7eb0-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="b7eb0-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b7eb0-116">**IRunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-116">**IRunActionCallback**</span></span>](/windows/desktop/direct3dtools/irunactioncallback)

 

 
