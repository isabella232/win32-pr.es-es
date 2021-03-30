---
description: Solicitudes para depurar un sombreador en la GPU (depuración en directo) vs CPU (depuración basada en seguimiento).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugLiveShaderRequest:: BeginDebugLiveShader (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806212"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="28e8d-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest:: BeginDebugLiveShader (método)</span><span class="sxs-lookup"><span data-stu-id="28e8d-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="28e8d-104">Solicitudes para depurar un sombreador en la GPU (depuración en directo) vs CPU (depuración basada en seguimiento).</span><span class="sxs-lookup"><span data-stu-id="28e8d-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="28e8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e8d-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="28e8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28e8d-106">Parameters</span></span>

<span data-ttu-id="28e8d-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="28e8d-107">*requestInfo* </span></span>  
<span data-ttu-id="28e8d-108">Dirección de una estructura DebugShaderRequestInfo que describe el evento, el vértice y el píxel solicitados.</span><span class="sxs-lookup"><span data-stu-id="28e8d-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="28e8d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28e8d-109">Return value</span></span>

<span data-ttu-id="28e8d-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="28e8d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28e8d-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28e8d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e8d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e8d-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="28e8d-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28e8d-113">Header</span></span></p></td><td><span data-ttu-id="28e8d-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="28e8d-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="28e8d-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="28e8d-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="28e8d-116">**IDebugLiveShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="28e8d-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
