---
description: '<span id="vspixengine.ipipelinestagescallback"></span>Interfaz IPipeLineStagesCallback: no se usa. Anteriormente, una devolución de llamada para los datos de las fases de canalización.'
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback (interfaz)
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
ms.openlocfilehash: 7782985f4317a02d2b159722f7a5897978b952b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087903"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="085f7-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="085f7-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="085f7-105">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="085f7-105">Not used.</span></span> <span data-ttu-id="085f7-106">Anteriormente, una devolución de llamada para los datos de las fases de canalización.</span><span class="sxs-lookup"><span data-stu-id="085f7-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="085f7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="085f7-107">Members</span></span>

<span data-ttu-id="085f7-108">La **interfaz IPipeLineStagesCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="085f7-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="085f7-109">**IPipeLineStagesCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="085f7-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="085f7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="085f7-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="085f7-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="085f7-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="085f7-112">La **interfaz IPipeLineStagesCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="085f7-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="085f7-113">Método</span><span class="sxs-lookup"><span data-stu-id="085f7-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="085f7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="085f7-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="085f7-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="085f7-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="085f7-116">Devolución de llamada que notifica al host qué fases de canalización se usan en la llamada a draw de la solicitud assocaited.</span><span class="sxs-lookup"><span data-stu-id="085f7-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="085f7-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="085f7-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="085f7-118">Devolución de llamada que notifica al host qué fases de canalización no pueden devolver datos de malla para el evento especificado en la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="085f7-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="085f7-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="085f7-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="085f7-120">Devolución de llamada que notifica al host la información de malla de fases de canalización devuelta por la solicitud assocaited.</span><span class="sxs-lookup"><span data-stu-id="085f7-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="085f7-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="085f7-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="085f7-122">Devolución de llamada que notifica al host la información de la imagen de las fases de canalización devuelta por la solicitud assocaited.</span><span class="sxs-lookup"><span data-stu-id="085f7-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="085f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="085f7-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="085f7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="085f7-124">Header</span></span></p></td><td><span data-ttu-id="085f7-125">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="085f7-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
