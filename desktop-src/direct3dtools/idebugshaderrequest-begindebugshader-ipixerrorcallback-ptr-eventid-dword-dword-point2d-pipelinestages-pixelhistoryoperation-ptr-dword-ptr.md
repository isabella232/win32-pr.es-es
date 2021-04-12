---
description: Solicita que inicie una sesión de depuración de sombreador para la fase de canalización especificada, píxel/vértice, si corresponde, evento y marco.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest:: BeginDebugShader (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152373"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="672c0-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest:: BeginDebugShader (método)</span><span class="sxs-lookup"><span data-stu-id="672c0-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="672c0-104">Solicita que inicie una sesión de depuración de sombreador para la fase de canalización especificada, píxel/vértice, si corresponde, evento y marco.</span><span class="sxs-lookup"><span data-stu-id="672c0-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="672c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="672c0-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="672c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="672c0-106">Parameters</span></span>

<span data-ttu-id="672c0-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="672c0-107">*errorCallback* </span></span>  
<span data-ttu-id="672c0-108">Dirección de una devolución de llamada para los errores que pueden producirse durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="672c0-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="672c0-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="672c0-109">*eventID* </span></span>  
<span data-ttu-id="672c0-110">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="672c0-110">The specified event.</span></span>

<span data-ttu-id="672c0-111">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="672c0-111">*frameNumber* </span></span>  
<span data-ttu-id="672c0-112">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="672c0-112">The specified frame.</span></span>

<span data-ttu-id="672c0-113">*vértice* </span><span class="sxs-lookup"><span data-stu-id="672c0-113">*vertex* </span></span>  
<span data-ttu-id="672c0-114">El vértice especificado.</span><span class="sxs-lookup"><span data-stu-id="672c0-114">The specified vertex.</span></span> <span data-ttu-id="672c0-115">Solo se aplica al depurar un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="672c0-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="672c0-116">*píxel* </span><span class="sxs-lookup"><span data-stu-id="672c0-116">*pixel* </span></span>  
<span data-ttu-id="672c0-117">Píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="672c0-117">The specified pixel.</span></span> <span data-ttu-id="672c0-118">Solo se aplica al depurar un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="672c0-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="672c0-119">*media* </span><span class="sxs-lookup"><span data-stu-id="672c0-119">*stage* </span></span>  
<span data-ttu-id="672c0-120">La fase de canalización especificada.</span><span class="sxs-lookup"><span data-stu-id="672c0-120">The specified pipeline stage.</span></span>

<span data-ttu-id="672c0-121">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="672c0-121">*pPixelHistory* </span></span>  
<span data-ttu-id="672c0-122">Dirección de los resultados del historial de píxeles utilizados para buscar el píxel asociado que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="672c0-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="672c0-123">Solo se aplica al depurar un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="672c0-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="672c0-124">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="672c0-124">*pDevice* </span></span>  
<span data-ttu-id="672c0-125">Dirección que se va a pasar al motor de depuración para comunicarse con esta sesión de depuración (motor de depuración readprocessmemory en esta dirección).</span><span class="sxs-lookup"><span data-stu-id="672c0-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="672c0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="672c0-126">Return value</span></span>

<span data-ttu-id="672c0-127">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="672c0-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="672c0-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="672c0-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="672c0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="672c0-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="672c0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="672c0-130">Header</span></span></p></td><td><span data-ttu-id="672c0-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="672c0-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="672c0-132"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="672c0-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="672c0-133">**IDebugShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="672c0-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
