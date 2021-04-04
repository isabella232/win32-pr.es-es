---
description: No se utiliza. Anteriormente era una devolución de llamada para los datos de etapas de canalización.
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPipeLineStagesCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997756"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="d7d36-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interfaz IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="d7d36-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="d7d36-105">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d7d36-105">Not used.</span></span> <span data-ttu-id="d7d36-106">Anteriormente era una devolución de llamada para los datos de etapas de canalización.</span><span class="sxs-lookup"><span data-stu-id="d7d36-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="d7d36-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7d36-107">Members</span></span>

<span data-ttu-id="d7d36-108">La interfaz **IPipeLineStagesCallback2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7d36-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7d36-109">**IPipeLineStagesCallback2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d7d36-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="d7d36-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7d36-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d7d36-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="d7d36-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d7d36-112">La interfaz **IPipeLineStagesCallback2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7d36-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d7d36-113">Método</span><span class="sxs-lookup"><span data-stu-id="d7d36-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d7d36-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7d36-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d7d36-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7d36-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d7d36-116">Devolución de llamada que notifica al host el número de subprocesos y grupos del sombreador de cálculo en la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="d7d36-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d7d36-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7d36-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d7d36-118">Devolución de llamada que notifica al host que ThreadData no está disponible para una fase de canalización y un evento determinados.</span><span class="sxs-lookup"><span data-stu-id="d7d36-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d7d36-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7d36-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d7d36-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7d36-120">Header</span></span></p></td><td><span data-ttu-id="d7d36-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d7d36-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
