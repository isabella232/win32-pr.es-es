---
description: Solicitudes para generar instrucciones de seguimiento del sombreador en una solicitud de depuración. La depuración basada en seguimiento se produce en la CPU (warp) en lugar de en la GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2:: GenerateInstructions (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537546"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="63414-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2:: GenerateInstructions (método)</span><span class="sxs-lookup"><span data-stu-id="63414-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="63414-105">Solicitudes para generar instrucciones de seguimiento del sombreador en una solicitud de depuración.</span><span class="sxs-lookup"><span data-stu-id="63414-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="63414-106">La depuración basada en seguimiento se produce en la CPU (warp) en lugar de en la GPU.</span><span class="sxs-lookup"><span data-stu-id="63414-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="63414-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63414-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="63414-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63414-108">Parameters</span></span>

<span data-ttu-id="63414-109">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="63414-109">*errorCallback* </span></span>  
<span data-ttu-id="63414-110">Dirección de una devolución de llamada para los errores que pueden producirse al generar las instrucciones de seguimiento del sombreador.</span><span class="sxs-lookup"><span data-stu-id="63414-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="63414-111">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="63414-111">*requestInfo* </span></span>  
<span data-ttu-id="63414-112">Dirección de una estructura DebugShaderRequestInfo que describe el evento, el vértice y el píxel solicitados.</span><span class="sxs-lookup"><span data-stu-id="63414-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="63414-113">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="63414-113">*pPixelHistory* </span></span>  
<span data-ttu-id="63414-114">Dirección de los resultados del historial de píxeles utilizados para buscar el píxel asociado que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="63414-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="63414-115">Solo se aplica al depurar un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="63414-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="63414-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="63414-116">*pCallback* </span></span>  
<span data-ttu-id="63414-117">La dirección de una devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="63414-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="63414-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63414-118">Return value</span></span>

<span data-ttu-id="63414-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="63414-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63414-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63414-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63414-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63414-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="63414-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63414-122">Header</span></span></p></td><td><span data-ttu-id="63414-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="63414-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="63414-124"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="63414-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="63414-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="63414-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
