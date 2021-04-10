---
description: Devolución de llamada para devolver el contenido de un objeto en formato de búfer para los que lo admiten (búferes, texturas).
MS-HAID: vspixengine.IBufferObjectDataCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IBufferObjectDataCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAE4CE9A-B8EB-4ED6-9F48-D00C19B27A2E
api_name:
- IBufferObjectDataCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e5fb7deebd7d1b16d333ae59edab9372b54ad8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152218"
---
# <a name="span-idvspixengineibufferobjectdatacallbackspanibufferobjectdatacallback-interface"></a><span data-ttu-id="c3d5e-103"><span id="vspixengine.ibufferobjectdatacallback"></span>Interfaz IBufferObjectDataCallback</span><span class="sxs-lookup"><span data-stu-id="c3d5e-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback interface</span></span>

<span data-ttu-id="c3d5e-104">Devolución de llamada para devolver el contenido de un objeto en formato de búfer para los que lo admiten (búferes, texturas).</span><span class="sxs-lookup"><span data-stu-id="c3d5e-104">Callback to return the contents of an object in buffer form for those that support it (buffers, textures).</span></span>

## <a name="members"></a><span data-ttu-id="c3d5e-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3d5e-105">Members</span></span>

<span data-ttu-id="c3d5e-106">La interfaz **IBufferObjectDataCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c3d5e-106">The **IBufferObjectDataCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c3d5e-107">**IBufferObjectDataCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c3d5e-107">**IBufferObjectDataCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c3d5e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3d5e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c3d5e-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c3d5e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c3d5e-110">La interfaz **IBufferObjectDataCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-110">The **IBufferObjectDataCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c3d5e-111">Método</span><span class="sxs-lookup"><span data-stu-id="c3d5e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c3d5e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3d5e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c3d5e-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="c3d5e-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c3d5e-114">Devolución de llamada que notifica al host la información del búfer escrita en un archivo mediante la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-114">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c3d5e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d5e-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c3d5e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3d5e-116">Header</span></span></p></td><td><span data-ttu-id="c3d5e-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c3d5e-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
