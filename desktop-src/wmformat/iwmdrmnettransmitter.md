---
title: Interfaz IWMDRMNetTransmitter
description: La interfaz IWMDRMNetTransmitter proporciona los métodos necesarios para usar DRM de Windows Media para dispositivos de red como transmisor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMNetTransmitter como parámetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Interfaz IWMDRMNetTransmitter formato de Windows Media
- Interfaz IWMDRMNetTransmitter formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359180"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="5b9c1-106">Interfaz IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="5b9c1-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="5b9c1-107">La interfaz **IWMDRMNetTransmitter** proporciona los métodos necesarios para usar DRM de Windows Media para dispositivos de red como transmisor.</span><span class="sxs-lookup"><span data-stu-id="5b9c1-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="5b9c1-108">Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="5b9c1-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="5b9c1-109">Pase el **IID \_ IWMDRMNetTransmitter** como parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="5b9c1-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="5b9c1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b9c1-110">Members</span></span>

<span data-ttu-id="5b9c1-111">La interfaz **IWMDRMNetTransmitter** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5b9c1-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5b9c1-112">**IWMDRMNetTransmitter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5b9c1-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="5b9c1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b9c1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5b9c1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b9c1-114">Methods</span></span>

<span data-ttu-id="5b9c1-115">La interfaz **IWMDRMNetTransmitter** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5b9c1-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="5b9c1-116">Método</span><span class="sxs-lookup"><span data-stu-id="5b9c1-116">Method</span></span>                                                                        | <span data-ttu-id="5b9c1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b9c1-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b9c1-118">**GetLeafLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="5b9c1-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="5b9c1-119">Genera un mensaje de respuesta de licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="5b9c1-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="5b9c1-120">**GetRootLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="5b9c1-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="5b9c1-121">Genera un mensaje de respuesta de licencia raíz</span><span class="sxs-lookup"><span data-stu-id="5b9c1-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="5b9c1-122">**SetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="5b9c1-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="5b9c1-123">Procesa un desafío de licencia enviado por un receptor de Microsoft Windows Media DRM para dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="5b9c1-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5b9c1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b9c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9c1-125">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="5b9c1-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5b9c1-126">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="5b9c1-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 

