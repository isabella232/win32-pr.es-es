---
description: Extensiones de la interfaz IPixEngine original.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494693"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="87e89-103"><span id="vspixengine.ipixengine2"></span>Interfaz IPixEngine2</span><span class="sxs-lookup"><span data-stu-id="87e89-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="87e89-104">Extensiones de la interfaz IPixEngine original.</span><span class="sxs-lookup"><span data-stu-id="87e89-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="87e89-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="87e89-105">Members</span></span>

<span data-ttu-id="87e89-106">La interfaz **IPixEngine2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="87e89-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87e89-107">**IPixEngine2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="87e89-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="87e89-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="87e89-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="87e89-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="87e89-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="87e89-110">La interfaz **IPixEngine2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="87e89-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="87e89-111">Método</span><span class="sxs-lookup"><span data-stu-id="87e89-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="87e89-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="87e89-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="87e89-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="87e89-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="87e89-114">Finaliza el experiement y completa el registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="87e89-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="87e89-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="87e89-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="87e89-116">Obtiene información sobre el equipo de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="87e89-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="87e89-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="87e89-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="87e89-118">Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.</span><span class="sxs-lookup"><span data-stu-id="87e89-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="87e89-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="87e89-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="87e89-120">Establece el equipo de reproducción actual para el registro de gráficos especificado.</span><span class="sxs-lookup"><span data-stu-id="87e89-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="87e89-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e89-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="87e89-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87e89-122">Header</span></span></p></td><td><span data-ttu-id="87e89-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="87e89-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
