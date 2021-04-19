---
description: Define los identificadores de recursos para los recursos de cadena compartidos.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537570"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span data-ttu-id="4cf13-103"><span id="vspixengine.resource_id"></span>\_Enumeración de ID. de recurso</span><span class="sxs-lookup"><span data-stu-id="4cf13-103"><span id="vspixengine.resource_id"></span>Resource\_Id enumeration</span></span>

<span data-ttu-id="4cf13-104">Define los identificadores de recursos para los recursos de cadena compartidos.</span><span class="sxs-lookup"><span data-stu-id="4cf13-104">Defines resource IDs for shared string resources.</span></span> <span data-ttu-id="4cf13-105">Estos se pasan al motor de captura desde el host.</span><span class="sxs-lookup"><span data-stu-id="4cf13-105">These are passed to the capture engine from the host.</span></span> <span data-ttu-id="4cf13-106">Se usan para mostrar cadenas en la superposición de HUD de la aplicación que se captura o para pasar valores de registro de las opciones de Visual Studio al engi de captura.</span><span class="sxs-lookup"><span data-stu-id="4cf13-106">They are used to display strings to the HUD overlay of the app being captured or to pass registry values from Visual Studio options to the capture engi</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf13-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cf13-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="4cf13-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="4cf13-108">Constants</span></span>

<span data-ttu-id="4cf13-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ID \_ ENGINEDISCONNECTED**</span><span class="sxs-lookup"><span data-stu-id="4cf13-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**IDS\_ENGINEDISCONNECTED**</span></span>  
<span data-ttu-id="4cf13-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-110">Not used.</span></span> <span data-ttu-id="4cf13-111">Identificador de recurso de la cadena que se ha usado anteriormente para indicar que se ha alcanzado PrintScreen una vez completada la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="4cf13-111">Resource id for string formerly used to indicate that printscreen was hit after the capture session was complete.</span></span>

<span data-ttu-id="4cf13-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**RCDATA1 de IDR \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR\_RCDATA1**</span></span>  
<span data-ttu-id="4cf13-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-113">Not used.</span></span>

<span data-ttu-id="4cf13-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**contenido de IDS \_ DEFAULTEXPFILE \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS\_DEFAULTEXPFILE\_CONTENT**</span></span>  
<span data-ttu-id="4cf13-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-115">Not used.</span></span> <span data-ttu-id="4cf13-116">Identificador de recurso de la cadena que se usó anteriormente para los datos XML en escenarios de captura heredados.</span><span class="sxs-lookup"><span data-stu-id="4cf13-116">Resource id for string formerly used for XML data in legacy capture scenarios.</span></span>

<span data-ttu-id="4cf13-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_mensaje de captura de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**IDS\_CAPTURE\_MESSAGE**</span></span>  
<span data-ttu-id="4cf13-118">IDENTIFICADOR de recurso para la cadena "Frame capturado".</span><span class="sxs-lookup"><span data-stu-id="4cf13-118">Resource ID for string "Captured frame."</span></span>

<span data-ttu-id="4cf13-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**\_no se \_ \_ admite la captura de IDS**</span><span class="sxs-lookup"><span data-stu-id="4cf13-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-120">IDENTIFICADOR de recurso de la cadena "este programa ha indicado que no se puede usar con herramientas de Diagnóstico de gráficos".</span><span class="sxs-lookup"><span data-stu-id="4cf13-120">Resource ID for string "This program has indicated that it cannot be used with Graphics Diagnostics tools."</span></span>

<span data-ttu-id="4cf13-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**título de captura de ID. \_ \_ no \_ admitido \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED\_TITLE**</span></span>  
<span data-ttu-id="4cf13-122">IDENTIFICADOR de recurso para la cadena "funcionalidad no admitida"</span><span class="sxs-lookup"><span data-stu-id="4cf13-122">Resource ID for string "Unsupported functionality"</span></span>

<span data-ttu-id="4cf13-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_no se \_ \_ admite la característica IDS**</span><span class="sxs-lookup"><span data-stu-id="4cf13-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**IDS\_FEATURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-124">IDENTIFICADOR de recurso para la cadena "no se admite el nivel de característica del dispositivo"</span><span class="sxs-lookup"><span data-stu-id="4cf13-124">Resource ID for string "Device feature level not supported"</span></span>

<span data-ttu-id="4cf13-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ID \_ DXVERSION \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="4cf13-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS\_DXVERSION\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-126">IDENTIFICADOR de recurso de la cadena "DirectX version not capturable"</span><span class="sxs-lookup"><span data-stu-id="4cf13-126">Resource ID for string "DirectX version not capturable"</span></span>

<span data-ttu-id="4cf13-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ID \_ DCOMP \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="4cf13-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**IDS\_DCOMP\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-128">IDENTIFICADOR de recurso de la cadena "DCOMP en uso por la aplicación, pero no compatible con este sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="4cf13-128">Resource ID for string "DCOMP in use by app but not supported on this OS"</span></span>

<span data-ttu-id="4cf13-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ID \_ DWRITE \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="4cf13-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS\_DWRITE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-130">IDENTIFICADOR de recurso de la cadena "DWRITE en uso por la aplicación, pero no compatible con este sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="4cf13-130">Resource ID for string "DWRITE in use by app but not supported on this OS"</span></span>

<span data-ttu-id="4cf13-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**formato de error de ID. \_ esperado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS\_EXPECTED\_FAILURE\_FORMAT**</span></span>  
<span data-ttu-id="4cf13-132">El ID. de recurso de la cadena "% s devolvió un error durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4cf13-132">Resource ID for string "%s returned an error during playback.</span></span> <span data-ttu-id="4cf13-133">(HRESULT =% s) \\ r \\ n ".</span><span class="sxs-lookup"><span data-stu-id="4cf13-133">(HRESULT=%s)\\r\\n".</span></span>

<span data-ttu-id="4cf13-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**mensaje de ID \_ CAPTURETOOLTIP \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE**</span></span>  
<span data-ttu-id="4cf13-135">IDENTIFICADOR de recurso para la cadena "use la tecla Impr Pant" para capturar un fotograma. "</span><span class="sxs-lookup"><span data-stu-id="4cf13-135">Resource ID for string "Use 'Print Screen' key to capture a frame."</span></span>

<span data-ttu-id="4cf13-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**\_No se \_ \_ \_ \_ admiten los identificadores D2D y D10**</span><span class="sxs-lookup"><span data-stu-id="4cf13-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS\_D2D\_AND\_D10\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="4cf13-137">El identificador de recurso de la cadena "D2D y D10 no se admite juntos en este sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="4cf13-137">Resource ID for string "D2D and D10 not supported together on this OS"</span></span>

<span data-ttu-id="4cf13-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**ID. de \_ HUD \_ estadísticas**</span><span class="sxs-lookup"><span data-stu-id="4cf13-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS\_HUD\_STATISTICS**</span></span>  
<span data-ttu-id="4cf13-139">IDENTIFICADOR de recurso para la cadena "fotogramas capturados% d.</span><span class="sxs-lookup"><span data-stu-id="4cf13-139">Resource ID for string "Frames captured %d.</span></span> <span data-ttu-id="4cf13-140">Tiempo de marco (MS)% 0,00 f "</span><span class="sxs-lookup"><span data-stu-id="4cf13-140">Frame time (ms) %0.00f"</span></span>

<span data-ttu-id="4cf13-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**ID \_ ( \_ método interno)**</span><span class="sxs-lookup"><span data-stu-id="4cf13-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS\_INTERNAL\_METHOD**</span></span>  
<span data-ttu-id="4cf13-142">IDENTIFICADOR de recurso para la cadena "método interno de DirectX"</span><span class="sxs-lookup"><span data-stu-id="4cf13-142">Resource ID for string "Directx Internal Method"</span></span>

<span data-ttu-id="4cf13-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_marca de \_ fotogramas de captura de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS\_CAPTURE\_FRAME\_MARK**</span></span>  
<span data-ttu-id="4cf13-144">IDENTIFICADOR de recurso para la cadena "fotograma capturado% LD"</span><span class="sxs-lookup"><span data-stu-id="4cf13-144">Resource ID for string "Captured Frame %ld"</span></span>

<span data-ttu-id="4cf13-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE\_INPUTASSEMBLER**</span></span>  
<span data-ttu-id="4cf13-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-146">Not used.</span></span>

<span data-ttu-id="4cf13-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE\_VERTEXSHADER**</span></span>  
<span data-ttu-id="4cf13-148">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-148">Not used.</span></span>

<span data-ttu-id="4cf13-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE\_HULLSHADER**</span></span>  
<span data-ttu-id="4cf13-150">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-150">Not used.</span></span>

<span data-ttu-id="4cf13-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**</span><span class="sxs-lookup"><span data-stu-id="4cf13-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE\_TESSELATOR**</span></span>  
<span data-ttu-id="4cf13-152">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-152">Not used.</span></span>

<span data-ttu-id="4cf13-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE\_DOMAINSHADER**</span></span>  
<span data-ttu-id="4cf13-154">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-154">Not used.</span></span>

<span data-ttu-id="4cf13-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE\_GEOMETRYSHADER**</span></span>  
<span data-ttu-id="4cf13-156">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-156">Not used.</span></span>

<span data-ttu-id="4cf13-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE\_STREAMOUTPUT**</span></span>  
<span data-ttu-id="4cf13-158">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-158">Not used.</span></span>

<span data-ttu-id="4cf13-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_rasterizador PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE\_RASTERIZER**</span></span>  
<span data-ttu-id="4cf13-160">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-160">Not used.</span></span>

<span data-ttu-id="4cf13-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ u**</span><span class="sxs-lookup"><span data-stu-id="4cf13-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE\_PIXELSHADER**</span></span>  
<span data-ttu-id="4cf13-162">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-162">Not used.</span></span>

<span data-ttu-id="4cf13-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE\_OUTPUTMERGER**</span></span>  
<span data-ttu-id="4cf13-164">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-164">Not used.</span></span>

<span data-ttu-id="4cf13-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE\_COMPUTESHADER**</span></span>  
<span data-ttu-id="4cf13-166">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-166">Not used.</span></span>

<span data-ttu-id="4cf13-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT\_SUPPORTEDFORMAT**</span></span>  
<span data-ttu-id="4cf13-168">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-168">Not used.</span></span>

<span data-ttu-id="4cf13-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT\_CURRENTFORMAT**</span></span>  
<span data-ttu-id="4cf13-170">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-170">Not used.</span></span>

<span data-ttu-id="4cf13-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_encabezado BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT\_HEADER**</span></span>  
<span data-ttu-id="4cf13-172">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-172">Not used.</span></span>

<span data-ttu-id="4cf13-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**\_línea BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT\_LINE**</span></span>  
<span data-ttu-id="4cf13-174">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-174">Not used.</span></span>

<span data-ttu-id="4cf13-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT\_INVALIDFORMAT**</span></span>  
<span data-ttu-id="4cf13-176">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-176">Not used.</span></span>

<span data-ttu-id="4cf13-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT\_INVALIDEMPTYFORMAT**</span></span>  
<span data-ttu-id="4cf13-178">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-178">Not used.</span></span>

<span data-ttu-id="4cf13-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT\_INVALIDFORMATSIZE**</span></span>  
<span data-ttu-id="4cf13-180">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-180">Not used.</span></span>

<span data-ttu-id="4cf13-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO\_TARGETAPPLICATION**</span></span>  
<span data-ttu-id="4cf13-182">Texto que se muestra en la ventana Propiedades de vsglog-aplicación de destino</span><span class="sxs-lookup"><span data-stu-id="4cf13-182">Text shown in the vsglog properties window - Target Application</span></span>

<span data-ttu-id="4cf13-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**la \_ ruta de acceso SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO\_PATH**</span></span>  
<span data-ttu-id="4cf13-184">Texto que se muestra en vsglog ventana Propiedades-path</span><span class="sxs-lookup"><span data-stu-id="4cf13-184">Text shown in the vsglog Properties window - Path</span></span>

<span data-ttu-id="4cf13-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO\_TARGETVERSION**</span></span>  
<span data-ttu-id="4cf13-186">Texto que se muestra en vsglog ventana Propiedades-versión de destino</span><span class="sxs-lookup"><span data-stu-id="4cf13-186">Text shown in the vsglog Properties window - Target Version</span></span>

<span data-ttu-id="4cf13-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LastModifiedDate & gt**</span><span class="sxs-lookup"><span data-stu-id="4cf13-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO\_LASTMODIFIEDDATE**</span></span>  
<span data-ttu-id="4cf13-188">Texto que se muestra en el ventana Propiedades vsglog: fecha de última modificación</span><span class="sxs-lookup"><span data-stu-id="4cf13-188">Text shown in the vsglog Properties window - Last Modified Date</span></span>

<span data-ttu-id="4cf13-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**no es el \_ PROCESSID**</span><span class="sxs-lookup"><span data-stu-id="4cf13-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO\_PROCESSID**</span></span>  
<span data-ttu-id="4cf13-190">Texto que se muestra en vsglog ventana Propiedades-Process ID</span><span class="sxs-lookup"><span data-stu-id="4cf13-190">Text shown in the vsglog Properties window - Process ID</span></span>

<span data-ttu-id="4cf13-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO\_EXPERIMENTFILE**</span></span>  
<span data-ttu-id="4cf13-192">Texto que se muestra en el archivo vsglog ventana Propiedades-experimento</span><span class="sxs-lookup"><span data-stu-id="4cf13-192">Text shown in the vsglog Properties window - Experiment File</span></span>

<span data-ttu-id="4cf13-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO\_RUNFILE**</span></span>  
<span data-ttu-id="4cf13-194">Texto que se muestra en el ventana Propiedades vsglog-Run File</span><span class="sxs-lookup"><span data-stu-id="4cf13-194">Text shown in the vsglog Properties window - Run File</span></span>

<span data-ttu-id="4cf13-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**tamaño de SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO\_SIZE**</span></span>  
<span data-ttu-id="4cf13-196">Texto que se muestra en vsglog ventana Propiedades-size</span><span class="sxs-lookup"><span data-stu-id="4cf13-196">Text shown in the vsglog Properties window - Size</span></span>

<span data-ttu-id="4cf13-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO\_CREATEDBYPIXVERSION**</span></span>  
<span data-ttu-id="4cf13-198">Texto que se muestra en el ventana Propiedades vsglog: creado por versión</span><span class="sxs-lookup"><span data-stu-id="4cf13-198">Text shown in the vsglog Properties window - Created By Version</span></span>

<span data-ttu-id="4cf13-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**</span><span class="sxs-lookup"><span data-stu-id="4cf13-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO\_SESSIONSTARTTIME**</span></span>  
<span data-ttu-id="4cf13-200">Texto que se muestra en la ventana Propiedades vsglog: hora de inicio de la sesión</span><span class="sxs-lookup"><span data-stu-id="4cf13-200">Text shown in the vsglog Properties window - Session Start time</span></span>

<span data-ttu-id="4cf13-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO\_SYSTEMINFORMATION**</span></span>  
<span data-ttu-id="4cf13-202">Texto que se muestra en la ventana Propiedades vsglog: información del sistema</span><span class="sxs-lookup"><span data-stu-id="4cf13-202">Text shown in the vsglog Properties window - System Information</span></span>

<span data-ttu-id="4cf13-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_procesador SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO\_PROCESSOR**</span></span>  
<span data-ttu-id="4cf13-204">Texto que se muestra en el procesador ventana Propiedades vsglog</span><span class="sxs-lookup"><span data-stu-id="4cf13-204">Text shown in the vsglog Properties window - Processor</span></span>

<span data-ttu-id="4cf13-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_memoria SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO\_MEMORY**</span></span>  
<span data-ttu-id="4cf13-206">Texto que se muestra en vsglog ventana Propiedades-Memory</span><span class="sxs-lookup"><span data-stu-id="4cf13-206">Text shown in the vsglog Properties window - Memory</span></span>

<span data-ttu-id="4cf13-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**no \_ es SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO\_OSVERSION**</span></span>  
<span data-ttu-id="4cf13-208">Texto que se muestra en la versión vsglog ventana Propiedades-OS</span><span class="sxs-lookup"><span data-stu-id="4cf13-208">Text shown in the vsglog Properties window - OS Version</span></span>

<span data-ttu-id="4cf13-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO\_OSARCHITECTURE**</span></span>  
<span data-ttu-id="4cf13-210">Texto que se muestra en la arquitectura vsglog ventana Propiedades-OS</span><span class="sxs-lookup"><span data-stu-id="4cf13-210">Text shown in the vsglog Properties window - OS Architecture</span></span>

<span data-ttu-id="4cf13-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO\_TARGETAPPARCHITECTURE**</span></span>  
<span data-ttu-id="4cf13-212">Texto que se muestra en la arquitectura de la aplicación vsglog ventana Propiedades-Target</span><span class="sxs-lookup"><span data-stu-id="4cf13-212">Text shown in the vsglog Properties window - Target App Architecture</span></span>

<span data-ttu-id="4cf13-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**</span><span class="sxs-lookup"><span data-stu-id="4cf13-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO\_MAXHWFEATURELEVEL**</span></span>  
<span data-ttu-id="4cf13-214">Texto que se muestra en el nivel de características de hardware ventana Propiedades vsglog-Max</span><span class="sxs-lookup"><span data-stu-id="4cf13-214">Text shown in the vsglog Properties window - Max Hardware Feature Level</span></span>

<span data-ttu-id="4cf13-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**</span><span class="sxs-lookup"><span data-stu-id="4cf13-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO\_DRIVERCONCURRENTCREATES**</span></span>  
<span data-ttu-id="4cf13-216">Texto que se muestra en el vsglog ventana Propiedades-driver crea de forma simultánea</span><span class="sxs-lookup"><span data-stu-id="4cf13-216">Text shown in the vsglog Properties window - Driver Concurrent Creates</span></span>

<span data-ttu-id="4cf13-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**</span><span class="sxs-lookup"><span data-stu-id="4cf13-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO\_DRIVERCOMMANDLISTS**</span></span>  
<span data-ttu-id="4cf13-218">Texto que se muestra en las listas de comandos de vsglog ventana Propiedades-driver</span><span class="sxs-lookup"><span data-stu-id="4cf13-218">Text shown in the vsglog Properties window - Driver Command Lists</span></span>

<span data-ttu-id="4cf13-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**</span><span class="sxs-lookup"><span data-stu-id="4cf13-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO\_DOUBLEPRECISIONSHADERS**</span></span>  
<span data-ttu-id="4cf13-220">Texto que se muestra en los sombreadores de precisión vsglog ventana Propiedades-Double</span><span class="sxs-lookup"><span data-stu-id="4cf13-220">Text shown in the vsglog Properties window - Double Precision Shaders</span></span>

<span data-ttu-id="4cf13-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**</span><span class="sxs-lookup"><span data-stu-id="4cf13-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO\_DIRECTCOMPUTECS4X**</span></span>  
<span data-ttu-id="4cf13-222">Texto que se muestra en vsglog ventana Propiedades-Direct Compute CS 4. x</span><span class="sxs-lookup"><span data-stu-id="4cf13-222">Text shown in the vsglog Properties window - Direct Compute CS 4.x</span></span>

<span data-ttu-id="4cf13-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO\_10BITXRHIGHCOLORFORMAT**</span></span>  
<span data-ttu-id="4cf13-224">Texto que se muestra en vsglog ventana Propiedades-10BITXRHIGHCOLORFORMAT</span><span class="sxs-lookup"><span data-stu-id="4cf13-224">Text shown in the vsglog Properties window - 10BITXRHIGHCOLORFORMAT</span></span>

<span data-ttu-id="4cf13-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO\_EXTENDEDCOLORFORMATSUPPORT**</span></span>  
<span data-ttu-id="4cf13-226">Texto que se muestra en la compatibilidad con el formato de color vsglog ventana Propiedades-Extended.</span><span class="sxs-lookup"><span data-stu-id="4cf13-226">Text shown in the vsglog Properties window - Extended Color Format Support</span></span>

<span data-ttu-id="4cf13-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO\_DISPLAYINFORMATION**</span></span>  
<span data-ttu-id="4cf13-228">Texto que se muestra en la ventana Propiedades de vsglog: Mostrar información</span><span class="sxs-lookup"><span data-stu-id="4cf13-228">Text shown in the vsglog Properties window - Display Information</span></span>

<span data-ttu-id="4cf13-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO\_DISPLAYNINFORMATION**</span></span>  
<span data-ttu-id="4cf13-230">Texto que se muestra en el ventana Propiedades vsglog-Mostrar N información</span><span class="sxs-lookup"><span data-stu-id="4cf13-230">Text shown in the vsglog Properties window - Display N Information</span></span>

<span data-ttu-id="4cf13-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**nombre de SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO\_NAME**</span></span>  
<span data-ttu-id="4cf13-232">Texto que se muestra en vsglog ventana Propiedades-Name</span><span class="sxs-lookup"><span data-stu-id="4cf13-232">Text shown in the vsglog Properties window - Name</span></span>

<span data-ttu-id="4cf13-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**Descripción de SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO\_DESCRIPTION**</span></span>  
<span data-ttu-id="4cf13-234">Texto que se muestra en el ventana Propiedades vsglog-Description</span><span class="sxs-lookup"><span data-stu-id="4cf13-234">Text shown in the vsglog Properties window - Description</span></span>

<span data-ttu-id="4cf13-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**</span><span class="sxs-lookup"><span data-stu-id="4cf13-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO\_DISPLAYMEMORY**</span></span>  
<span data-ttu-id="4cf13-236">Texto que se muestra en el ventana Propiedades vsglog-Mostrar memoria</span><span class="sxs-lookup"><span data-stu-id="4cf13-236">Text shown in the vsglog Properties window - Display Memory</span></span>

<span data-ttu-id="4cf13-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**</span><span class="sxs-lookup"><span data-stu-id="4cf13-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO\_DRIVERNAME**</span></span>  
<span data-ttu-id="4cf13-238">Texto que se muestra en el vsglog ventana Propiedades-nombre del controlador</span><span class="sxs-lookup"><span data-stu-id="4cf13-238">Text shown in the vsglog Properties window - Driver Name</span></span>

<span data-ttu-id="4cf13-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO\_DRIVERVERSION**</span></span>  
<span data-ttu-id="4cf13-240">Texto que se muestra en la versión de vsglog ventana Propiedades-driver</span><span class="sxs-lookup"><span data-stu-id="4cf13-240">Text shown in the vsglog Properties window - Driver Version</span></span>

<span data-ttu-id="4cf13-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO\_MODULEINFORMATION**</span></span>  
<span data-ttu-id="4cf13-242">Texto que se muestra en la información de vsglog ventana Propiedades-Module</span><span class="sxs-lookup"><span data-stu-id="4cf13-242">Text shown in the vsglog Properties window - Module Information</span></span>

<span data-ttu-id="4cf13-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO\_DIRECT3DINFORMATION**</span></span>  
<span data-ttu-id="4cf13-244">Texto que se muestra en la información de ventana Propiedades vsglog-Direct3D</span><span class="sxs-lookup"><span data-stu-id="4cf13-244">Text shown in the vsglog Properties window - Direct3D Information</span></span>

<span data-ttu-id="4cf13-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO\_VSGVERSION**</span></span>  
<span data-ttu-id="4cf13-246">Texto que se muestra en la versión vsglog ventana Propiedades-VSG</span><span class="sxs-lookup"><span data-stu-id="4cf13-246">Text shown in the vsglog Properties window - VSG Version</span></span>

<span data-ttu-id="4cf13-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO\_CAPTUREMACHINE**</span></span>  
<span data-ttu-id="4cf13-248">Texto que se muestra en la máquina vsglog ventana Propiedades-Capture</span><span class="sxs-lookup"><span data-stu-id="4cf13-248">Text shown in the vsglog Properties window - Capture Machine</span></span>

<span data-ttu-id="4cf13-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO\_PLAYBACKMACHINE**</span></span>  
<span data-ttu-id="4cf13-250">Texto que se muestra en la máquina de ventana Propiedades-reproducción de vsglog</span><span class="sxs-lookup"><span data-stu-id="4cf13-250">Text shown in the vsglog Properties window - Playback Machine</span></span>

<span data-ttu-id="4cf13-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**\_REMOTEDATA SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO\_REMOTEDATA**</span></span>  
<span data-ttu-id="4cf13-252">Texto que se muestra en el ventana Propiedades de vsglog-datos remotos</span><span class="sxs-lookup"><span data-stu-id="4cf13-252">Text shown in the vsglog Properties window - Remote Data</span></span>

<span data-ttu-id="4cf13-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**</span><span class="sxs-lookup"><span data-stu-id="4cf13-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO\_OtherDirect3DInformation**</span></span>  
<span data-ttu-id="4cf13-254">Texto que se muestra en vsglog ventana Propiedades-otra información de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4cf13-254">Text shown in the vsglog Properties window - Other Direct3D Information</span></span>

<span data-ttu-id="4cf13-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**</span><span class="sxs-lookup"><span data-stu-id="4cf13-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO\_SIZEGB**</span></span>  
<span data-ttu-id="4cf13-256">Texto que se muestra en el vsglog de tamaño ventana Propiedades GB</span><span class="sxs-lookup"><span data-stu-id="4cf13-256">Text shown in the vsglog Properties window - Size GB</span></span>

<span data-ttu-id="4cf13-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**</span><span class="sxs-lookup"><span data-stu-id="4cf13-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO\_SIZEMB**</span></span>  
<span data-ttu-id="4cf13-258">Texto que se muestra en vsglog ventana Propiedades-size MB</span><span class="sxs-lookup"><span data-stu-id="4cf13-258">Text shown in the vsglog Properties window - Size MB</span></span>

<span data-ttu-id="4cf13-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ bytes**</span><span class="sxs-lookup"><span data-stu-id="4cf13-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO\_SIZEBYTES**</span></span>  
<span data-ttu-id="4cf13-260">Texto que se muestra en vsglog ventana Propiedades-size bytes</span><span class="sxs-lookup"><span data-stu-id="4cf13-260">Text shown in the vsglog Properties window - Size Bytes</span></span>

<span data-ttu-id="4cf13-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**</span><span class="sxs-lookup"><span data-stu-id="4cf13-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO\_MEMORYMB**</span></span>  
<span data-ttu-id="4cf13-262">Texto que se muestra en vsglog ventana Propiedades-Memory MB</span><span class="sxs-lookup"><span data-stu-id="4cf13-262">Text shown in the vsglog Properties window - Memory MB</span></span>

<span data-ttu-id="4cf13-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ x86**</span><span class="sxs-lookup"><span data-stu-id="4cf13-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO\_X86**</span></span>  
<span data-ttu-id="4cf13-264">Texto que se muestra en el ventana Propiedades vsglog-x86</span><span class="sxs-lookup"><span data-stu-id="4cf13-264">Text shown in the vsglog Properties window - X86</span></span>

<span data-ttu-id="4cf13-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ x64**</span><span class="sxs-lookup"><span data-stu-id="4cf13-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO\_X64**</span></span>  
<span data-ttu-id="4cf13-266">Texto que se muestra en vsglog ventana Propiedades-x64</span><span class="sxs-lookup"><span data-stu-id="4cf13-266">Text shown in the vsglog Properties window - X64</span></span>

<span data-ttu-id="4cf13-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ true**</span><span class="sxs-lookup"><span data-stu-id="4cf13-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO\_TRUE**</span></span>  
<span data-ttu-id="4cf13-268">Texto que se muestra en vsglog ventana Propiedades-true</span><span class="sxs-lookup"><span data-stu-id="4cf13-268">Text shown in the vsglog Properties window - True</span></span>

<span data-ttu-id="4cf13-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ false**</span><span class="sxs-lookup"><span data-stu-id="4cf13-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO\_FALSE**</span></span>  
<span data-ttu-id="4cf13-270">Texto que se muestra en el ventana Propiedades vsglog-false</span><span class="sxs-lookup"><span data-stu-id="4cf13-270">Text shown in the vsglog Properties window - False</span></span>

<span data-ttu-id="4cf13-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**</span><span class="sxs-lookup"><span data-stu-id="4cf13-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO\_ARM32**</span></span>  
<span data-ttu-id="4cf13-272">Texto que se muestra en vsglog ventana Propiedades-ARM 32</span><span class="sxs-lookup"><span data-stu-id="4cf13-272">Text shown in the vsglog Properties window - ARM 32</span></span>

<span data-ttu-id="4cf13-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO\_UNKNOWNCPUARCHITECTURE**</span></span>  
<span data-ttu-id="4cf13-274">Texto que se muestra en vsglog ventana Propiedades: arquitectura de CPU desconocida</span><span class="sxs-lookup"><span data-stu-id="4cf13-274">Text shown in the vsglog Properties window - Unknown CPU Architecture</span></span>

<span data-ttu-id="4cf13-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**</span><span class="sxs-lookup"><span data-stu-id="4cf13-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO\_AllDXGIFormatValues**</span></span>  
<span data-ttu-id="4cf13-276">Texto que se muestra en el ventana Propiedades vsglog: todos los valores de formato de DXGI</span><span class="sxs-lookup"><span data-stu-id="4cf13-276">Text shown in the vsglog Properties window - All DXGI Format Values</span></span>

<span data-ttu-id="4cf13-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**</span><span class="sxs-lookup"><span data-stu-id="4cf13-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO\_AllD3D11FormatSupportValues**</span></span>  
<span data-ttu-id="4cf13-278">Texto que se muestra en el formato vsglog ventana Propiedades-All D3D11 support Values</span><span class="sxs-lookup"><span data-stu-id="4cf13-278">Text shown in the vsglog Properties window - All D3D11 Format Support Values</span></span>

<span data-ttu-id="4cf13-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**Subprocesamiento de \_ características de D3D11 SUMMARYINFO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO\_D3D11\_FEATURE\_THREADING**</span></span>  
<span data-ttu-id="4cf13-280">Texto que se muestra en el subproceso de la característica vsglog ventana Propiedades-D3D11 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-280">Text shown in the vsglog Properties window - D3D11\_FEATURE\_THREADING</span></span>

<span data-ttu-id="4cf13-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO\_DriverConcurrentCreates1**</span></span>  
<span data-ttu-id="4cf13-282">El texto que se muestra en el vsglog ventana Propiedades-driver crea 1</span><span class="sxs-lookup"><span data-stu-id="4cf13-282">Text shown in the vsglog Properties window - Driver Concurrent Creates 1</span></span>

<span data-ttu-id="4cf13-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO\_DriverCommandLists1**</span></span>  
<span data-ttu-id="4cf13-284">Texto que se muestra en el comando vsglog ventana Propiedades-driver lists 1</span><span class="sxs-lookup"><span data-stu-id="4cf13-284">Text shown in the vsglog Properties window - Driver Command Lists 1</span></span>

<span data-ttu-id="4cf13-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**Los \_ \_ dobles de características de D3D11 SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO\_D3D11\_FEATURE\_DOUBLES**</span></span>  
<span data-ttu-id="4cf13-286">El texto que se muestra en la característica vsglog ventana Propiedades-D3D11 se \_ \_ duplica</span><span class="sxs-lookup"><span data-stu-id="4cf13-286">Text shown in the vsglog Properties window - D3D11\_FEATURE\_DOUBLES</span></span>

<span data-ttu-id="4cf13-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**</span><span class="sxs-lookup"><span data-stu-id="4cf13-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO\_DoublePrecisionFloatShaderOps**</span></span>  
<span data-ttu-id="4cf13-288">Texto que se muestra en las operaciones vsglog ventana Propiedades-Double precisión Float Shader</span><span class="sxs-lookup"><span data-stu-id="4cf13-288">Text shown in the vsglog Properties window - Double Precision Float Shader Ops</span></span>

<span data-ttu-id="4cf13-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Opciones de hardware \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**</span></span>  
<span data-ttu-id="4cf13-290">Texto que se muestra en vsglog ventana Propiedades- \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Opciones de hardware</span><span class="sxs-lookup"><span data-stu-id="4cf13-290">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS</span></span>

<span data-ttu-id="4cf13-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ a través del \_ sombreador \_ 4 \_ x**</span><span class="sxs-lookup"><span data-stu-id="4cf13-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO\_ComputeShaders\_Plus\_RawAndStructuredBuffers\_Via\_Shader\_4\_x**</span></span>  
<span data-ttu-id="4cf13-292">Texto que se muestra en vsglog ventana Propiedades-ComputeShaders + RAW y Structure dBuffers a través del sombreador 4. x</span><span class="sxs-lookup"><span data-stu-id="4cf13-292">Text shown in the vsglog Properties window - ComputeShaders + Raw and Structure dBuffers via Shader 4.x</span></span>

<span data-ttu-id="4cf13-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**Opciones de D3D11 de la \_ característica de D3D11 SUMMARYINFO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS**</span></span>  
<span data-ttu-id="4cf13-294">Texto que se muestra en las opciones de vsglog ventana Propiedades-D3D11 de la \_ característica \_ D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-294">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS</span></span>

<span data-ttu-id="4cf13-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**</span><span class="sxs-lookup"><span data-stu-id="4cf13-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO\_OutputMergerLogicOp**</span></span>  
<span data-ttu-id="4cf13-296">Texto que se muestra en la vsglog de la lógica de combinación de salida ventana Propiedades-Output</span><span class="sxs-lookup"><span data-stu-id="4cf13-296">Text shown in the vsglog Properties window - Output Merger Logic Op</span></span>

<span data-ttu-id="4cf13-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**</span><span class="sxs-lookup"><span data-stu-id="4cf13-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO\_UAVOnlyRenderingForcedSampleCount**</span></span>  
<span data-ttu-id="4cf13-298">Texto que se muestra en el recuento de muestras forzada de vsglog ventana Propiedades-UAV</span><span class="sxs-lookup"><span data-stu-id="4cf13-298">Text shown in the vsglog Properties window - UAV Only Rendering Forced Sample Count</span></span>

<span data-ttu-id="4cf13-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**</span><span class="sxs-lookup"><span data-stu-id="4cf13-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO\_DiscardAPIsSeenByDriver**</span></span>  
<span data-ttu-id="4cf13-300">Texto que se muestra en las API vsglog ventana Propiedades-discard que ve el controlador</span><span class="sxs-lookup"><span data-stu-id="4cf13-300">Text shown in the vsglog Properties window - Discard APIs Seen By Driver</span></span>

<span data-ttu-id="4cf13-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**</span><span class="sxs-lookup"><span data-stu-id="4cf13-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO\_FlagsForUpdateAndCopySeenByDriver**</span></span>  
<span data-ttu-id="4cf13-302">Texto que se muestra en el vsglog ventana Propiedades: marcas de actualización y copia que ve el controlador</span><span class="sxs-lookup"><span data-stu-id="4cf13-302">Text shown in the vsglog Properties window - Flags For Update And Copy Seen By Driver</span></span>

<span data-ttu-id="4cf13-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ Clearview**</span><span class="sxs-lookup"><span data-stu-id="4cf13-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO\_ClearView**</span></span>  
<span data-ttu-id="4cf13-304">Texto que se muestra en la vista ventana Propiedades-Clear de vsglog</span><span class="sxs-lookup"><span data-stu-id="4cf13-304">Text shown in the vsglog Properties window - Clear View</span></span>

<span data-ttu-id="4cf13-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**</span><span class="sxs-lookup"><span data-stu-id="4cf13-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO\_CopyWithOverlap**</span></span>  
<span data-ttu-id="4cf13-306">Texto que se muestra en vsglog ventana Propiedades-Copy with superposición</span><span class="sxs-lookup"><span data-stu-id="4cf13-306">Text shown in the vsglog Properties window - Copy With Overlap</span></span>

<span data-ttu-id="4cf13-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**</span><span class="sxs-lookup"><span data-stu-id="4cf13-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO\_ConstantBufferPartialUpdate**</span></span>  
<span data-ttu-id="4cf13-308">Texto que se muestra en la actualización parcial del búfer vsglog ventana Propiedades-Constant</span><span class="sxs-lookup"><span data-stu-id="4cf13-308">Text shown in the vsglog Properties window - Constant Buffer Partial Update</span></span>

<span data-ttu-id="4cf13-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**</span><span class="sxs-lookup"><span data-stu-id="4cf13-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO\_ConstantBufferOffsetting**</span></span>  
<span data-ttu-id="4cf13-310">Texto que se muestra en el desplazamiento del búfer vsglog ventana Propiedades-Constant</span><span class="sxs-lookup"><span data-stu-id="4cf13-310">Text shown in the vsglog Properties window - Constant Buffer Offsetting</span></span>

<span data-ttu-id="4cf13-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="4cf13-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicConstantBuffer**</span></span>  
<span data-ttu-id="4cf13-312">Texto que se muestra en la ventana Propiedades de vsglog: no sobrescribir en el búfer de constantes dinámicas</span><span class="sxs-lookup"><span data-stu-id="4cf13-312">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Constant Buffer</span></span>

<span data-ttu-id="4cf13-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**</span><span class="sxs-lookup"><span data-stu-id="4cf13-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicBufferSRV**</span></span>  
<span data-ttu-id="4cf13-314">Texto que se muestra en la ventana Propiedades vsglog: no sobrescribir en el SRV de búfer dinámico</span><span class="sxs-lookup"><span data-stu-id="4cf13-314">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Buffer SRV</span></span>

<span data-ttu-id="4cf13-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**</span><span class="sxs-lookup"><span data-stu-id="4cf13-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO\_MultisampleRTVWithForcedSampleCountOne**</span></span>  
<span data-ttu-id="4cf13-316">Texto que se muestra en vsglog ventana Propiedades-Multisample RTV con el recuento de muestras forzadas uno</span><span class="sxs-lookup"><span data-stu-id="4cf13-316">Text shown in the vsglog Properties window - Multisample RTV With Forced Sample Count One</span></span>

<span data-ttu-id="4cf13-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**</span><span class="sxs-lookup"><span data-stu-id="4cf13-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO\_SAD4ShaderInstructions**</span></span>  
<span data-ttu-id="4cf13-318">Texto que se muestra en las instrucciones del sombreador vsglog ventana Propiedades-SAD4</span><span class="sxs-lookup"><span data-stu-id="4cf13-318">Text shown in the vsglog Properties window - SAD4 Shader Instructions</span></span>

<span data-ttu-id="4cf13-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**</span><span class="sxs-lookup"><span data-stu-id="4cf13-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO\_ExtendedDoublesShaderInstructions**</span></span>  
<span data-ttu-id="4cf13-320">Texto que se muestra en las instrucciones del sombreador de ventana Propiedades vsglog-Extended Double</span><span class="sxs-lookup"><span data-stu-id="4cf13-320">Text shown in the vsglog Properties window - Extended Doubles Shader Instructions</span></span>

<span data-ttu-id="4cf13-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**</span><span class="sxs-lookup"><span data-stu-id="4cf13-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO\_ExtendedResourceSharing**</span></span>  
<span data-ttu-id="4cf13-322">Texto que se muestra en el ventana Propiedades vsglog: uso compartido de recursos extendidos</span><span class="sxs-lookup"><span data-stu-id="4cf13-322">Text shown in the vsglog Properties window - Extended Resource Sharing</span></span>

<span data-ttu-id="4cf13-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_Información de \_ arquitectura de características de D3D11 SUMMARYINFO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO\_D3D11\_FEATURE\_ARCHITECTURE\_INFO**</span></span>  
<span data-ttu-id="4cf13-324">Texto que se muestra en la información de \_ arquitectura de características de vsglog ventana Propiedades-D3D11 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-324">Text shown in the vsglog Properties window - D3D11\_FEATURE\_ARCHITECTURE\_INFO</span></span>

<span data-ttu-id="4cf13-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**</span><span class="sxs-lookup"><span data-stu-id="4cf13-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO\_TileBasedDeferredRenderer**</span></span>  
<span data-ttu-id="4cf13-326">Texto que se muestra en el representador diferido ventana Propiedades vsglog en mosaico</span><span class="sxs-lookup"><span data-stu-id="4cf13-326">Text shown in the vsglog Properties window - Tile Based Deferred Renderer</span></span>

<span data-ttu-id="4cf13-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**Opciones de D3D9 de la \_ característica de D3D11 SUMMARYINFO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS**</span></span>  
<span data-ttu-id="4cf13-328">Texto que se muestra en las opciones de vsglog ventana Propiedades-D3D11 de la \_ característica \_ D3D9 \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-328">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS</span></span>

<span data-ttu-id="4cf13-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**</span><span class="sxs-lookup"><span data-stu-id="4cf13-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO\_FullNonPow2TextureSupport**</span></span>  
<span data-ttu-id="4cf13-330">Texto que se muestra en la ventana Propiedades vsglog-Full Texture no Pow2</span><span class="sxs-lookup"><span data-stu-id="4cf13-330">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Support</span></span>

<span data-ttu-id="4cf13-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**\_ \_ \_ \_ \_ Compatibilidad con la precisión mínima del sombreador de características de D3D11 SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT**</span></span>  
<span data-ttu-id="4cf13-332">Texto que se muestra en la \_ \_ \_ \_ compatibilidad con la precisión mínima del sombreador de características de vsglog ventana Propiedades-D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-332">Text shown in the vsglog Properties window - D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT</span></span>

<span data-ttu-id="4cf13-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**</span><span class="sxs-lookup"><span data-stu-id="4cf13-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO\_PixelShaderMinPrecision**</span></span>  
<span data-ttu-id="4cf13-334">Texto que se muestra en la precisión mínima del sombreador de ventana Propiedades de vsglog de píxeles</span><span class="sxs-lookup"><span data-stu-id="4cf13-334">Text shown in the vsglog Properties window - Pixel Shader Min Precision</span></span>

<span data-ttu-id="4cf13-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**</span><span class="sxs-lookup"><span data-stu-id="4cf13-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO\_AllOtherShaderStagesMinPrecision**</span></span>  
<span data-ttu-id="4cf13-336">Texto que se muestra en el ventana Propiedades vsglog-todas las demás etapas del sombreador precisión mínima</span><span class="sxs-lookup"><span data-stu-id="4cf13-336">Text shown in the vsglog Properties window - All Other Shader Stages Min Precision</span></span>

<span data-ttu-id="4cf13-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**D3D11, la \_ \_ característica de \_ D3D9 \_ Shadow \_ support**</span><span class="sxs-lookup"><span data-stu-id="4cf13-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT**</span></span>  
<span data-ttu-id="4cf13-338">Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ características de \_ \_ \_ compatibilidad con instantáneas D3D9</span><span class="sxs-lookup"><span data-stu-id="4cf13-338">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT</span></span>

<span data-ttu-id="4cf13-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**</span><span class="sxs-lookup"><span data-stu-id="4cf13-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO\_SupportsDepthAsTextureWithLessEqualComparisonFilter**</span></span>  
<span data-ttu-id="4cf13-340">Texto que se muestra en el ventana Propiedades vsglog: admite la profundidad como textura con un filtro de comparación menos idéntico.</span><span class="sxs-lookup"><span data-stu-id="4cf13-340">Text shown in the vsglog Properties window - Supports Depth As Texture With Less Equal Comparison Filter</span></span>

<span data-ttu-id="4cf13-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ característica \_ D3D11 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS1**</span></span>  
<span data-ttu-id="4cf13-342">Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D11 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="4cf13-342">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS1</span></span>

<span data-ttu-id="4cf13-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**</span><span class="sxs-lookup"><span data-stu-id="4cf13-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO\_TiledResourcesTier**</span></span>  
<span data-ttu-id="4cf13-344">Texto que se muestra en el nivel de vsglog ventana Propiedades de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="4cf13-344">Text shown in the vsglog Properties window - Tiled Resources Tier</span></span>

<span data-ttu-id="4cf13-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**</span><span class="sxs-lookup"><span data-stu-id="4cf13-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO\_MinMaxFiltering**</span></span>  
<span data-ttu-id="4cf13-346">Texto que se muestra en vsglog ventana Propiedades-Min Max Filtering</span><span class="sxs-lookup"><span data-stu-id="4cf13-346">Text shown in the vsglog Properties window - Min Max Filtering</span></span>

<span data-ttu-id="4cf13-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**</span><span class="sxs-lookup"><span data-stu-id="4cf13-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO\_ClearViewAlsoSupportsDepthOnlyFormats**</span></span>  
<span data-ttu-id="4cf13-348">El texto que se muestra en la vista ventana Propiedades-Clear de vsglog también admite formatos solo de profundidad</span><span class="sxs-lookup"><span data-stu-id="4cf13-348">Text shown in the vsglog Properties window - Clear View Also Supports Depth Only Formats</span></span>

<span data-ttu-id="4cf13-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**</span><span class="sxs-lookup"><span data-stu-id="4cf13-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO\_MapOnDefaultBuffers**</span></span>  
<span data-ttu-id="4cf13-350">Texto que se muestra en el mapa de ventana Propiedades de vsglog en los búferes predeterminados</span><span class="sxs-lookup"><span data-stu-id="4cf13-350">Text shown in the vsglog Properties window - Map On Default Buffers</span></span>

<span data-ttu-id="4cf13-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**La \_ característica de D3D11 de la creación de instancias de D3D9 es \_ \_ \_ \_ \_ compatible.**</span><span class="sxs-lookup"><span data-stu-id="4cf13-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT**</span></span>  
<span data-ttu-id="4cf13-352">Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D9 \_ \_ compatibilidad con la creación de instancias simples \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-352">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT</span></span>

<span data-ttu-id="4cf13-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**</span><span class="sxs-lookup"><span data-stu-id="4cf13-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO\_SimpleInstancingSupported0**</span></span>  
<span data-ttu-id="4cf13-354">Texto que se muestra en la ventana Propiedades vsglog: se admite la creación de instancias simples 0</span><span class="sxs-lookup"><span data-stu-id="4cf13-354">Text shown in the vsglog Properties window - Simple Instancing Supported 0</span></span>

<span data-ttu-id="4cf13-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_ \_ \_ Compatibilidad con el marcador de características de D3D11 SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_MARKER\_SUPPORT**</span></span>  
<span data-ttu-id="4cf13-356">Texto que se muestra en la \_ \_ compatibilidad con el marcador de características vsglog ventana Propiedades-D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="4cf13-356">Text shown in the vsglog Properties window - D3D11\_FEATURE\_MARKER\_SUPPORT</span></span>

<span data-ttu-id="4cf13-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Perfil SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO\_Profile**</span></span>  
<span data-ttu-id="4cf13-358">Texto que se muestra en vsglog ventana Propiedades-Profile</span><span class="sxs-lookup"><span data-stu-id="4cf13-358">Text shown in the vsglog Properties window - Profile</span></span>

<span data-ttu-id="4cf13-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ característica \_ D3D9 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS1**</span></span>  
<span data-ttu-id="4cf13-360">Texto que se muestra en la característica vsglog ventana Propiedades-D3D11 \_ \_ D3D9 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="4cf13-360">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS1</span></span>

<span data-ttu-id="4cf13-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**</span><span class="sxs-lookup"><span data-stu-id="4cf13-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO\_FullNonPow2TextureSupported**</span></span>  
<span data-ttu-id="4cf13-362">Texto que se muestra en la vsglog ventana Propiedades-Full Texture no Pow2 compatible</span><span class="sxs-lookup"><span data-stu-id="4cf13-362">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Supported</span></span>

<span data-ttu-id="4cf13-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**</span><span class="sxs-lookup"><span data-stu-id="4cf13-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO\_DepthAsTextureWithLessEqualComparisonFilterSupported**</span></span>  
<span data-ttu-id="4cf13-364">Texto que se muestra en vsglog ventana Propiedades-Depth como Texture con un filtro de comparación menos idéntico compatible</span><span class="sxs-lookup"><span data-stu-id="4cf13-364">Text shown in the vsglog Properties window - Depth As Texture With Less Equal Comparison Filter Supported</span></span>

<span data-ttu-id="4cf13-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO\_SimpleInstancingSupported1**</span></span>  
<span data-ttu-id="4cf13-366">Texto que se muestra en la ventana Propiedades vsglog: se admite la creación de instancias simples 1</span><span class="sxs-lookup"><span data-stu-id="4cf13-366">Text shown in the vsglog Properties window - Simple Instancing Supported 1</span></span>

<span data-ttu-id="4cf13-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span><span class="sxs-lookup"><span data-stu-id="4cf13-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO\_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span></span>  
<span data-ttu-id="4cf13-368">Texto que se muestra en el destino de representación de la esfera de vsglog ventana Propiedades-Texture con la galería de símbolos de profundidad sin cubo compatible</span><span class="sxs-lookup"><span data-stu-id="4cf13-368">Text shown in the vsglog Properties window - Texture Cube Face Render Target With Non-Cube Depth Stencil Supported</span></span>

<span data-ttu-id="4cf13-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**</span><span class="sxs-lookup"><span data-stu-id="4cf13-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO\_DXGIFormat**</span></span>  
<span data-ttu-id="4cf13-370">Texto que se muestra en vsglog ventana Propiedades-DXGIFormat</span><span class="sxs-lookup"><span data-stu-id="4cf13-370">Text shown in the vsglog Properties window - DXGIFormat</span></span>

<span data-ttu-id="4cf13-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**</span><span class="sxs-lookup"><span data-stu-id="4cf13-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO\_DXGIFormat1**</span></span>  
<span data-ttu-id="4cf13-372">Texto que se muestra en vsglog ventana Propiedades-DXGIFormat1</span><span class="sxs-lookup"><span data-stu-id="4cf13-372">Text shown in the vsglog Properties window - DXGIFormat1</span></span>

<span data-ttu-id="4cf13-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**\_MODULENAME SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="4cf13-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO\_MODULENAME**</span></span>  
<span data-ttu-id="4cf13-374">Texto que se muestra en vsglog ventana Propiedades-MODULENAME</span><span class="sxs-lookup"><span data-stu-id="4cf13-374">Text shown in the vsglog Properties window - MODULENAME</span></span>

<span data-ttu-id="4cf13-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**configuración de IDD \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD\_CONFIGURATION**</span></span>  
<span data-ttu-id="4cf13-376">Texto que se muestra en el cuadro de diálogo configurar Firewall en el VsGraphicsRemoteEngine</span><span class="sxs-lookup"><span data-stu-id="4cf13-376">Text shown in the Configure Firewall dialog in the VsGraphicsRemoteEngine</span></span>

<span data-ttu-id="4cf13-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_icono de \_ encabezado \_ estático IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC\_STATIC\_HEADER\_ICON**</span></span>  
<span data-ttu-id="4cf13-378">Texto que se muestra en el icono control de cuadro de diálogo configurar Firewall: encabezado estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-378">Text shown in the Configure Firewall dialog control - Static Header Icon</span></span>

<span data-ttu-id="4cf13-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_encabezado estático \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="4cf13-380">Texto que se muestra en el encabezado de control de cuadro de diálogo configurar Firewall: estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-380">Text shown in the Configure Firewall dialog control - Static Header</span></span>

<span data-ttu-id="4cf13-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_configuración de \_ FW \_ estático de IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC\_STATIC\_FW\_CONFIGURATION**</span></span>  
<span data-ttu-id="4cf13-382">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: configuración de Firewall estática</span><span class="sxs-lookup"><span data-stu-id="4cf13-382">Text shown in the Configure Firewall dialog control - Static Firewall Configuration</span></span>

<span data-ttu-id="4cf13-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_icono de \_ FW \_ estático de IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC\_STATIC\_FW\_ICON**</span></span>  
<span data-ttu-id="4cf13-384">Texto que se muestra en el icono de control de cuadro de diálogo configurar Firewall: estático Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-384">Text shown in the Configure Firewall dialog control - Static Firewall Icon</span></span>

<span data-ttu-id="4cf13-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_encabezado de \_ FW \_ estático de IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="4cf13-386">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: encabezado de Firewall estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-386">Text shown in the Configure Firewall dialog control - Static Firewall Header</span></span>

<span data-ttu-id="4cf13-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_firmware de \_ GROUPBOX \_ estático de IDC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="4cf13-388">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: firewall de GroupBox estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-388">Text shown in the Configure Firewall dialog control - Static Groupbox Firewall</span></span>

<span data-ttu-id="4cf13-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC, \_ comprobar las redes de \_ dominio de FW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-390">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar redes de dominio de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-390">Text shown in the Configure Firewall dialog control - Check Firewall Domain Networks</span></span>

<span data-ttu-id="4cf13-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC, \_ comprobación de \_ \_ redes privadas de FW \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-392">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar las redes privadas del firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-392">Text shown in the Configure Firewall dialog control - Check Firewall Private Networks</span></span>

<span data-ttu-id="4cf13-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC, \_ comprobar las \_ \_ redes públicas de FW \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-394">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: comprobar redes públicas de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-394">Text shown in the Configure Firewall dialog control - Check Firewall Public Networks</span></span>

<span data-ttu-id="4cf13-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**botón de IDC \_ \_ configurar**</span><span class="sxs-lookup"><span data-stu-id="4cf13-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="4cf13-396">Texto que se muestra en el control de cuadro de diálogo configurar Firewall: botón Configurar</span><span class="sxs-lookup"><span data-stu-id="4cf13-396">Text shown in the Configure Firewall dialog control - Button Configure</span></span>

<span data-ttu-id="4cf13-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**\_cancelación de configuración de ID. \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="4cf13-398">Texto que se muestra en el control de cuadro de diálogo configurar Firewall-configuración cancelar</span><span class="sxs-lookup"><span data-stu-id="4cf13-398">Text shown in the Configure Firewall dialog control - Configuration Cancel</span></span>

<span data-ttu-id="4cf13-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**firmware de texto de IDS \_ \_ \_ no \_ configurado**</span><span class="sxs-lookup"><span data-stu-id="4cf13-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS\_TEXT\_FW\_NOT\_CONFIGURED**</span></span>  
<span data-ttu-id="4cf13-400">Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de texto no configurado</span><span class="sxs-lookup"><span data-stu-id="4cf13-400">Text shown in the Configure Firewall dialog - Text Firewall Not Configured</span></span>

<span data-ttu-id="4cf13-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**firmware de texto de ID. \_ \_ \_ configurado**</span><span class="sxs-lookup"><span data-stu-id="4cf13-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS\_TEXT\_FW\_CONFIGURED**</span></span>  
<span data-ttu-id="4cf13-402">Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de texto configurado</span><span class="sxs-lookup"><span data-stu-id="4cf13-402">Text shown in the Configure Firewall dialog - Text Firewall Configured</span></span>

<span data-ttu-id="4cf13-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**\_nombre de \_ regla de Firewall de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS\_FIREWALL\_RULE\_NAME**</span></span>  
<span data-ttu-id="4cf13-404">Texto que se muestra en el cuadro de diálogo configurar Firewall: nombre de la regla de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-404">Text shown in the Configure Firewall dialog - Firewall Rule Name</span></span>

<span data-ttu-id="4cf13-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**Descripción de la regla de Firewall de IDS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS\_FIREWALL\_RULE\_DESCRIPTION**</span></span>  
<span data-ttu-id="4cf13-406">Texto que se muestra en el cuadro de diálogo configurar Firewall: Descripción de la regla de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-406">Text shown in the Configure Firewall dialog - Firewall Rule Description</span></span>

<span data-ttu-id="4cf13-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_encabezado estático de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**IDS\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="4cf13-408">Texto que se muestra en el encabezado del cuadro de diálogo configurar Firewall: estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-408">Text shown in the Configure Firewall dialog - Static Header</span></span>

<span data-ttu-id="4cf13-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_título de configuración de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**IDS\_CONFIGURATION\_TITLE**</span></span>  
<span data-ttu-id="4cf13-410">Texto que se muestra en el cuadro de diálogo configurar Firewall: título de configuración</span><span class="sxs-lookup"><span data-stu-id="4cf13-410">Text shown in the Configure Firewall dialog - Configuration Title</span></span>

<span data-ttu-id="4cf13-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**ID. de \_ \_ encabezado de FW estático \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**IDS\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="4cf13-412">Texto que se muestra en el cuadro de diálogo configurar Firewall: encabezado de Firewall estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-412">Text shown in the Configure Firewall dialog - Static Firewall Header</span></span>

<span data-ttu-id="4cf13-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDENTIFICADOres de \_ GROUPBOX de GROUPBOX estáticos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="4cf13-414">Texto que se muestra en el cuadro de diálogo configurar Firewall: firewall de GroupBox estático</span><span class="sxs-lookup"><span data-stu-id="4cf13-414">Text shown in the Configure Firewall dialog - Static Groupbox Firewall</span></span>

<span data-ttu-id="4cf13-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDENTIFICADOres \_ comprobar \_ redes de dominio de FW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-416">Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes de dominio de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-416">Text shown in the Configure Firewall dialog - Check Firewall Domain Networks</span></span>

<span data-ttu-id="4cf13-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDENTIFICADOres \_ comprobar \_ \_ redes privadas de FW \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-418">Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes privadas de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-418">Text shown in the Configure Firewall dialog - Check Firewall Private Networks</span></span>

<span data-ttu-id="4cf13-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDENTIFICADOres \_ comprobar \_ \_ redes públicas de FW \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="4cf13-420">Texto que se muestra en el cuadro de diálogo configurar Firewall: comprobar redes públicas de Firewall</span><span class="sxs-lookup"><span data-stu-id="4cf13-420">Text shown in the Configure Firewall dialog - Check Firewall public Networks</span></span>

<span data-ttu-id="4cf13-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**botón de identificación \_ \_ configurar**</span><span class="sxs-lookup"><span data-stu-id="4cf13-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**IDS\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="4cf13-422">Texto que se muestra en el cuadro de diálogo configurar Firewall-buttom Confiture</span><span class="sxs-lookup"><span data-stu-id="4cf13-422">Text shown in the Configure Firewall dialog - Buttom Confiture</span></span>

<span data-ttu-id="4cf13-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**configuración de ID. \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="4cf13-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**IDS\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="4cf13-424">Texto que se muestra en el cuadro de diálogo configurar Firewall-configuración cancelar</span><span class="sxs-lookup"><span data-stu-id="4cf13-424">Text shown in the Configure Firewall dialog - Configuration Cancel</span></span>

<span data-ttu-id="4cf13-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ID \_ CAPTURETOOLTIP \_ Message \_ CORESYSTEM**</span><span class="sxs-lookup"><span data-stu-id="4cf13-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE\_CORESYSTEM**</span></span>  
<span data-ttu-id="4cf13-426">IDENTIFICADOR de recurso para la cadena "use el botón capturar de Visual Studio para capturar fotogramas".</span><span class="sxs-lookup"><span data-stu-id="4cf13-426">Resource ID for string "Use the capture button in Visual Studio to capture frame(s)."</span></span>

<span data-ttu-id="4cf13-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDENTIFICADOres y \_ \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="4cf13-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS\_ET\_NONE**</span></span>  
<span data-ttu-id="4cf13-428">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-428">Not used.</span></span>

<span data-ttu-id="4cf13-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ID. \_ et \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="4cf13-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS\_ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="4cf13-430">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-430">Not used.</span></span>

<span data-ttu-id="4cf13-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ID. \_ et \_ SESSIONEND**</span><span class="sxs-lookup"><span data-stu-id="4cf13-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS\_ET\_SESSIONEND**</span></span>  
<span data-ttu-id="4cf13-432">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-432">Not used.</span></span>

<span data-ttu-id="4cf13-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ID. \_ et \_ PROCESSSTART**</span><span class="sxs-lookup"><span data-stu-id="4cf13-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS\_ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="4cf13-434">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-434">Not used.</span></span>

<span data-ttu-id="4cf13-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ID. \_ et \_ PROCESSEND**</span><span class="sxs-lookup"><span data-stu-id="4cf13-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS\_ET\_PROCESSEND**</span></span>  
<span data-ttu-id="4cf13-436">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-436">Not used.</span></span>

<span data-ttu-id="4cf13-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ID. \_ et \_ FRAMEBEGIN**</span><span class="sxs-lookup"><span data-stu-id="4cf13-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS\_ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="4cf13-438">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-438">Not used.</span></span>

<span data-ttu-id="4cf13-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ID. \_ et \_ FRAMEEND**</span><span class="sxs-lookup"><span data-stu-id="4cf13-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS\_ET\_FRAMEEND**</span></span>  
<span data-ttu-id="4cf13-440">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-440">Not used.</span></span>

<span data-ttu-id="4cf13-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ID. \_ et \_ USEREVENTBEGIN**</span><span class="sxs-lookup"><span data-stu-id="4cf13-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS\_ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="4cf13-442">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-442">Not used.</span></span>

<span data-ttu-id="4cf13-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ID. \_ et \_ USEREVENTEND**</span><span class="sxs-lookup"><span data-stu-id="4cf13-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS\_ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="4cf13-444">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-444">Not used.</span></span>

<span data-ttu-id="4cf13-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ID. \_ et \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS\_ET\_USERMARKER**</span></span>  
<span data-ttu-id="4cf13-446">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-446">Not used.</span></span>

<span data-ttu-id="4cf13-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID. \_ et \_ llamada**</span><span class="sxs-lookup"><span data-stu-id="4cf13-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS\_ET\_CALL**</span></span>  
<span data-ttu-id="4cf13-448">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-448">Not used.</span></span>

<span data-ttu-id="4cf13-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ID. \_ et \_ OBJECTPOPULATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS\_ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="4cf13-450">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-450">Not used.</span></span>

<span data-ttu-id="4cf13-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ID. \_ et \_ OBJECTCREATION**</span><span class="sxs-lookup"><span data-stu-id="4cf13-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS\_ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="4cf13-452">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-452">Not used.</span></span>

<span data-ttu-id="4cf13-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ID. \_ et \_ CALLSYNC**</span><span class="sxs-lookup"><span data-stu-id="4cf13-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS\_ET\_CALLSYNC**</span></span>  
<span data-ttu-id="4cf13-454">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-454">Not used.</span></span>

<span data-ttu-id="4cf13-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDENTIFICADOres \_ et \_ desconocidos**</span><span class="sxs-lookup"><span data-stu-id="4cf13-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS\_ET\_UNKNOWN**</span></span>  
<span data-ttu-id="4cf13-456">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-456">Not used.</span></span>

<span data-ttu-id="4cf13-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDENTIFICADOR no \_ desencadenar \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="4cf13-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS\_TRIGGER\_NONE**</span></span>  
<span data-ttu-id="4cf13-458">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-458">Not used.</span></span>

<span data-ttu-id="4cf13-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDENTIFICADOR de \_ desencadenador \_ PROGRAMSTART**</span><span class="sxs-lookup"><span data-stu-id="4cf13-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS\_TRIGGER\_PROGRAMSTART**</span></span>  
<span data-ttu-id="4cf13-460">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-460">Not used.</span></span>

<span data-ttu-id="4cf13-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_marco de desencadenador de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**IDS\_TRIGGER\_FRAME**</span></span>  
<span data-ttu-id="4cf13-462">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-462">Not used.</span></span>

<span data-ttu-id="4cf13-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_tiempo de desencadenamiento de IDS \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**IDS\_TRIGGER\_TIME**</span></span>  
<span data-ttu-id="4cf13-464">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-464">Not used.</span></span>

<span data-ttu-id="4cf13-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDENTIFICADOR de \_ desencadenador \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="4cf13-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS\_TRIGGER\_USERMARKER**</span></span>  
<span data-ttu-id="4cf13-466">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-466">Not used.</span></span>

<span data-ttu-id="4cf13-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDENTIFICADOR de \_ desencadenador \_ BEGINUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS\_TRIGGER\_BEGINUSEREVENT**</span></span>  
<span data-ttu-id="4cf13-468">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-468">Not used.</span></span>

<span data-ttu-id="4cf13-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDENTIFICADOR de \_ desencadenador \_ ENDUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="4cf13-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS\_TRIGGER\_ENDUSEREVENT**</span></span>  
<span data-ttu-id="4cf13-470">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-470">Not used.</span></span>

<span data-ttu-id="4cf13-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDENTIFICADOR de \_ desencadenador \_ CAPTUREFRAME**</span><span class="sxs-lookup"><span data-stu-id="4cf13-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS\_TRIGGER\_CAPTUREFRAME**</span></span>  
<span data-ttu-id="4cf13-472">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-472">Not used.</span></span>

<span data-ttu-id="4cf13-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDENTIFICADOR de \_ desencadenador \_ APICAPTURE**</span><span class="sxs-lookup"><span data-stu-id="4cf13-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS\_TRIGGER\_APICAPTURE**</span></span>  
<span data-ttu-id="4cf13-474">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-474">Not used.</span></span>

<span data-ttu-id="4cf13-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ERROR de ID \_ \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="4cf13-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**IDS\_ERROR\_CALLDATA**</span></span>  
<span data-ttu-id="4cf13-476">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-476">Not used.</span></span>

<span data-ttu-id="4cf13-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ERROR de ID \_ \_ CREATINGLOG**</span><span class="sxs-lookup"><span data-stu-id="4cf13-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**IDS\_ERROR\_CREATINGLOG**</span></span>  
<span data-ttu-id="4cf13-478">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-478">Not used.</span></span>

<span data-ttu-id="4cf13-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ID \_ UNKNOWNCALL**</span><span class="sxs-lookup"><span data-stu-id="4cf13-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS\_UNKNOWNCALL**</span></span>  
<span data-ttu-id="4cf13-480">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-480">Not used.</span></span>

<span data-ttu-id="4cf13-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**nivel de característica de advertencia de ID. \_ \_ \_ \_ cambiado**</span><span class="sxs-lookup"><span data-stu-id="4cf13-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS\_WARN\_FEATURE\_LEVEL\_CHANGED**</span></span>  
<span data-ttu-id="4cf13-482">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4cf13-482">Not used.</span></span>

<span data-ttu-id="4cf13-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_frecuencia de estado de ID. \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**ID\_STATUS\_FREQUENCY**</span></span>  

<span data-ttu-id="4cf13-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ deshabilitar \_ HUD**</span><span class="sxs-lookup"><span data-stu-id="4cf13-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID\_DISABLE\_HUD**</span></span>  

<span data-ttu-id="4cf13-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**IDENTIFICADOR \_ deshabilitar \_ compatibilidad**</span><span class="sxs-lookup"><span data-stu-id="4cf13-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID\_DISABLE\_COMPAT**</span></span>  

<span data-ttu-id="4cf13-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ recopilar \_ pilas**</span><span class="sxs-lookup"><span data-stu-id="4cf13-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID\_COLLECT\_CALLSTACKS**</span></span>  

<span data-ttu-id="4cf13-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**IDENTIFICADOR \_ habilitar \_ detención de SDKERROR \_**</span><span class="sxs-lookup"><span data-stu-id="4cf13-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID\_ENABLE\_SDKERROR\_STOP**</span></span>  

## <a name="requirements"></a><span data-ttu-id="4cf13-488">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf13-488">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4cf13-489">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cf13-489">Header</span></span></p></td><td><span data-ttu-id="4cf13-490">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4cf13-490">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



