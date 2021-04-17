---
title: Entrega previa de licencias
description: Entrega previa de licencias
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- SDK de Windows Media Format, entrega previa de licencias
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), entrega previa de licencias
- DRM (administración de derechos digitales), entrega previa de licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, entrega previa de licencias
- API extendidas de cliente, entrega previa de licencias
- entrega previa de licencias
- licencias, entrega previa de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656383"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="c2130-113">Entrega previa de licencias</span><span class="sxs-lookup"><span data-stu-id="c2130-113">License Pre-Delivery</span></span>

<span data-ttu-id="c2130-114">La entrega previa de licencias es el proceso que se usa para extraer las licencias a un equipo cliente de forma preferente.</span><span class="sxs-lookup"><span data-stu-id="c2130-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="c2130-115">Un escenario común para usar la entrega previa es cuando un usuario se suscribe a un servicio de música.</span><span class="sxs-lookup"><span data-stu-id="c2130-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="c2130-116">Sin ofrecer licencias antes de que sean necesarias, el usuario tendría que esperar la adquisición de licencias para cada nueva canción.</span><span class="sxs-lookup"><span data-stu-id="c2130-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="c2130-117">Dado que la entrega previa no se realiza como respuesta al intento de acceso, normalmente solo la realiza el propietario del contenido.</span><span class="sxs-lookup"><span data-stu-id="c2130-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="c2130-118">Es decir, solo puede proporcionar licencias previas para el contenido que usted controla.</span><span class="sxs-lookup"><span data-stu-id="c2130-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="c2130-119">El proceso de preventa es una coordinación entre un componente de cliente y un servidor de licencias creado mediante los objetos del SDK de Rights Management digital de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c2130-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="c2130-120">La entrega previa de licencias es similar a [la adquisición de licencias no silenciosa](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="c2130-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="c2130-121">Siga los mismos pasos, excepto que no tiene un encabezado DRM para pasar a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span><span class="sxs-lookup"><span data-stu-id="c2130-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="c2130-122">El método generará un desafío que no es específico del contenido y que puede enviar al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="c2130-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="c2130-123">También puede usar el administrador de [derechos de Windows Media](/previous-versions//bb676133(v=technet.10)) para proporcionar licencias previamente.</span><span class="sxs-lookup"><span data-stu-id="c2130-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2130-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2130-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2130-125">**Adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="c2130-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="c2130-126">**Usar el modelo de eventos Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="c2130-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 