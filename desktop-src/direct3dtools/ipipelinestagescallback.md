---
description: No se utiliza. Anteriormente era una devolución de llamada para los datos de etapas de canalización.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906840"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="38e7a-104"><span id="vspixengine.ipipelinestagescallback"></span>Interfaz IPipeLineStagesCallback</span><span class="sxs-lookup"><span data-stu-id="38e7a-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="38e7a-105">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="38e7a-105">Not used.</span></span> <span data-ttu-id="38e7a-106">Anteriormente era una devolución de llamada para los datos de etapas de canalización.</span><span class="sxs-lookup"><span data-stu-id="38e7a-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="38e7a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="38e7a-107">Members</span></span>

<span data-ttu-id="38e7a-108">La interfaz **IPipeLineStagesCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="38e7a-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="38e7a-109">**IPipeLineStagesCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="38e7a-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="38e7a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="38e7a-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="38e7a-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="38e7a-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="38e7a-112">La interfaz **IPipeLineStagesCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="38e7a-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="38e7a-113">Método</span><span class="sxs-lookup"><span data-stu-id="38e7a-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="38e7a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="38e7a-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="38e7a-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="38e7a-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="38e7a-116">Devolución de llamada que notifica al host las fases de canalización que usa la llamada a Draw de la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="38e7a-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="38e7a-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="38e7a-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="38e7a-118">Devolución de llamada que notifica al host las fases de canalización que no pueden devolver datos de malla para el evento especificado en la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="38e7a-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="38e7a-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="38e7a-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="38e7a-120">Devolución de llamada que notifica al host de las fases de canalización de la información de malla devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="38e7a-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="38e7a-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="38e7a-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="38e7a-122">Devolución de llamada que notifica al host la información de la imagen de las fases de canalización devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="38e7a-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="38e7a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e7a-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="38e7a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38e7a-124">Header</span></span></p></td><td><span data-ttu-id="38e7a-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="38e7a-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
