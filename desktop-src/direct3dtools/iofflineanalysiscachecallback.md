---
description: Devolución de llamada para devolver información sobre si una solicitud sin conexión se almacena en caché o no.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IOfflineAnalysisCacheCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E226B1A6-D028-4562-9C8C-D25EC91A2DB2
api_name:
- IOfflineAnalysisCacheCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e0107f97353bf7ad5b62472bc54a2b8388fb6aff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537929"
---
# <a name="span-idvspixengineiofflineanalysiscachecallbackspaniofflineanalysiscachecallback-interface"></a><span data-ttu-id="c41d6-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>Interfaz IOfflineAnalysisCacheCallback</span><span class="sxs-lookup"><span data-stu-id="c41d6-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback interface</span></span>

<span data-ttu-id="c41d6-104">Devolución de llamada para devolver información sobre si una solicitud sin conexión se almacena en caché o no.</span><span class="sxs-lookup"><span data-stu-id="c41d6-104">Callback to return information on whether an offline request is cached or not.</span></span>

## <a name="members"></a><span data-ttu-id="c41d6-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c41d6-105">Members</span></span>

<span data-ttu-id="c41d6-106">La interfaz **IOfflineAnalysisCacheCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c41d6-106">The **IOfflineAnalysisCacheCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c41d6-107">**IOfflineAnalysisCacheCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c41d6-107">**IOfflineAnalysisCacheCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c41d6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c41d6-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c41d6-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c41d6-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c41d6-110">La interfaz **IOfflineAnalysisCacheCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c41d6-110">The **IOfflineAnalysisCacheCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c41d6-111">Método</span><span class="sxs-lookup"><span data-stu-id="c41d6-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c41d6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c41d6-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c41d6-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="c41d6-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c41d6-114">Función de devolución de llamada que se usa para notificar al host qué Marcos tienen informes de análisis sin conexión disponibles.</span><span class="sxs-lookup"><span data-stu-id="c41d6-114">A callback function used to notify the host about which frames have offline analysis reports available.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c41d6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c41d6-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c41d6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c41d6-116">Header</span></span></p></td><td><span data-ttu-id="c41d6-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c41d6-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
