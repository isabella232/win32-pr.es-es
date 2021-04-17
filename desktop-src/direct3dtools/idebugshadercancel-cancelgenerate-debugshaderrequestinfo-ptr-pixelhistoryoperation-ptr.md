---
description: Solicita la cancelación de la generación de instrucciones de seguimiento del sombreador en una solicitud de depuración.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderCancel:: CancelGenerate (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705211"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="604ed-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel:: CancelGenerate (método)</span><span class="sxs-lookup"><span data-stu-id="604ed-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="604ed-104">Solicita la cancelación de la generación de instrucciones de seguimiento del sombreador en una solicitud de depuración.</span><span class="sxs-lookup"><span data-stu-id="604ed-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="604ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="604ed-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="604ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="604ed-106">Parameters</span></span>

<span data-ttu-id="604ed-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="604ed-107">*requestInfo* </span></span>  
<span data-ttu-id="604ed-108">Dirección de una estructura DebugShaderRequestInfo que describe el evento, el vértice y el píxel solicitados.</span><span class="sxs-lookup"><span data-stu-id="604ed-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="604ed-109">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="604ed-109">*pPixelHistory* </span></span>  
<span data-ttu-id="604ed-110">Dirección de los resultados del historial de píxeles utilizados para buscar el píxel asociado que se va a depurar.</span><span class="sxs-lookup"><span data-stu-id="604ed-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="604ed-111">Solo se aplica al depurar un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="604ed-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="604ed-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="604ed-112">Return value</span></span>

<span data-ttu-id="604ed-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="604ed-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="604ed-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="604ed-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="604ed-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="604ed-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="604ed-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="604ed-116">Header</span></span></p></td><td><span data-ttu-id="604ed-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="604ed-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="604ed-118"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="604ed-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="604ed-119">**IDebugShaderCancel**</span><span class="sxs-lookup"><span data-stu-id="604ed-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
