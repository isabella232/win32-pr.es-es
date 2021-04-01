---
description: Solicitar datos de análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IOfflineAnalysisRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 980c4d9f3b745d197789e5e450e0bf782127ca0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906751"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span data-ttu-id="be919-103"><span id="vspixengine.iofflineanalysisrequest"></span>Interfaz IOfflineAnalysisRequest</span><span class="sxs-lookup"><span data-stu-id="be919-103"><span id="vspixengine.iofflineanalysisrequest"></span>IOfflineAnalysisRequest interface</span></span>

<span data-ttu-id="be919-104">Solicitar datos de análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="be919-104">Request for offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="be919-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="be919-105">Members</span></span>

<span data-ttu-id="be919-106">La interfaz **IOfflineAnalysisRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be919-106">The **IOfflineAnalysisRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be919-107">**IOfflineAnalysisRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="be919-107">**IOfflineAnalysisRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="be919-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="be919-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="be919-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="be919-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="be919-110">La interfaz **IOfflineAnalysisRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="be919-110">The **IOfflineAnalysisRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="be919-111">Método</span><span class="sxs-lookup"><span data-stu-id="be919-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="be919-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="be919-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="be919-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="be919-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="be919-114">Solicitudes para cancelar el análisis sin conexión en una solicitud de análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="be919-114">Requests to cancel offline analysis in an offline analysis request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="be919-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="be919-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="be919-116">Solicita que se ejecute el análisis sin conexión con el origen especificado, el manifiesto, los parámetros y el marco especificado.</span><span class="sxs-lookup"><span data-stu-id="be919-116">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="be919-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be919-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="be919-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be919-118">Header</span></span></p></td><td><span data-ttu-id="be919-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="be919-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
