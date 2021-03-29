---
title: Interfaz IWMDRMNetReceiver
description: La interfaz IWMDRMNetReceiver proporciona los métodos necesarios para usar DRM de Microsoft Windows Media para dispositivos de red como receptor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMNetReceiver como parámetro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Interfaz IWMDRMNetReceiver formato de Windows Media
- Interfaz IWMDRMNetReceiver formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419733"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="84353-106">Interfaz IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="84353-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="84353-107">La interfaz **IWMDRMNetReceiver** proporciona los métodos necesarios para usar DRM de Microsoft Windows Media para dispositivos de red como receptor.</span><span class="sxs-lookup"><span data-stu-id="84353-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="84353-108">Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="84353-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="84353-109">Pase el **IID \_ IWMDRMNetReceiver** como parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="84353-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="84353-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="84353-110">Members</span></span>

<span data-ttu-id="84353-111">La interfaz **IWMDRMNetReceiver** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="84353-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="84353-112">**IWMDRMNetReceiver** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="84353-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="84353-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="84353-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84353-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="84353-114">Methods</span></span>

<span data-ttu-id="84353-115">La interfaz **IWMDRMNetReceiver** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="84353-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="84353-116">Método</span><span class="sxs-lookup"><span data-stu-id="84353-116">Method</span></span>                                                                               | <span data-ttu-id="84353-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="84353-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84353-118">**GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="84353-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="84353-119">Genera un desafío de licencia que se envía al transmisor al solicitar contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="84353-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="84353-120">**GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="84353-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="84353-121">Genera un desafío de registro que se envía al transmisor cuando el receptor se registra o se vuelve a validar.</span><span class="sxs-lookup"><span data-stu-id="84353-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="84353-122">**ProcessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="84353-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="84353-123">Procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="84353-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="84353-124">**ProcessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="84353-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="84353-125">Procesa la respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.</span><span class="sxs-lookup"><span data-stu-id="84353-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="84353-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="84353-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84353-127">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="84353-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="84353-128">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="84353-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="84353-129">**Interfaz IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="84353-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





