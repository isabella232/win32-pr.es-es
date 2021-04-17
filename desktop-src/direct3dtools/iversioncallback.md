---
description: Devolución de llamada para devolver las versiones de todas las interfaces admitidas. Esto permite que el consumidor no esté sincronizado con el motor de captura.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IVersionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705220"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="f818d-104"><span id="vspixengine.iversioncallback"></span>Interfaz IVersionCallback</span><span class="sxs-lookup"><span data-stu-id="f818d-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="f818d-105">Devolución de llamada para devolver las versiones de todas las interfaces admitidas.</span><span class="sxs-lookup"><span data-stu-id="f818d-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="f818d-106">Esto permite que el consumidor no esté sincronizado con el motor de captura.</span><span class="sxs-lookup"><span data-stu-id="f818d-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="f818d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f818d-107">Members</span></span>

<span data-ttu-id="f818d-108">La interfaz **IVersionCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f818d-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f818d-109">**IVersionCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f818d-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f818d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f818d-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f818d-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="f818d-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f818d-112">La interfaz **IVersionCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f818d-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f818d-113">Método</span><span class="sxs-lookup"><span data-stu-id="f818d-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f818d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f818d-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f818d-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span><span class="sxs-lookup"><span data-stu-id="f818d-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f818d-116">Función de devolución de llamada que se usa para notificar al host qué interfaces se admiten.</span><span class="sxs-lookup"><span data-stu-id="f818d-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f818d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f818d-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f818d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f818d-118">Header</span></span></p></td><td><span data-ttu-id="f818d-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f818d-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
