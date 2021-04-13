---
title: BasicDevice. Icons (propiedad)
description: Obtiene un vector de interfaces IDeviceIcon.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- Propiedad Icons media streaming API
- Propiedad Icons media streaming API, BasicDevice (interfaz)
- Interfaz BasicDevice API de streaming de multimedia, propiedad Icons
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420685"
---
# <a name="basicdeviceicons-property"></a><span data-ttu-id="19ddf-106">BasicDevice. Icons (propiedad)</span><span class="sxs-lookup"><span data-stu-id="19ddf-106">BasicDevice.Icons property</span></span>

<span data-ttu-id="19ddf-107">Obtiene un vector de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="19ddf-107">Gets a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

<span data-ttu-id="19ddf-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19ddf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ddf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19ddf-109">Syntax</span></span>


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a><span data-ttu-id="19ddf-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="19ddf-110">Property value</span></span>

<span data-ttu-id="19ddf-111">Colección enumerable de punteros de interfaz [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="19ddf-111">An enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

## <a name="see-also"></a><span data-ttu-id="19ddf-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="19ddf-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="19ddf-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19ddf-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

 