---
title: Interfaces de cliente DRM de Microsoft Windows Media
description: Interfaces de cliente DRM de Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- SDK de Windows Media Format, interfaces
- Administración de derechos digitales (DRM), interfaces
- DRM (administración de derechos digitales), interfaces
- API extendidas del cliente DRM, interfaces
- API extendidas del cliente, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421774"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="6276b-108">Interfaces de cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="6276b-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="6276b-109">En la tabla siguiente se describen las interfaces compatibles con las API de cliente de Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="6276b-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="6276b-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6276b-110">Interface</span></span>                                                                    | <span data-ttu-id="6276b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6276b-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6276b-112">**IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="6276b-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="6276b-113">Proporciona la definición de una devolución de llamada de estado que se puede implementar para controlar las operaciones DRM asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="6276b-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="6276b-114">**IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="6276b-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="6276b-115">Proporciona un método para descifrar el contenido.</span><span class="sxs-lookup"><span data-stu-id="6276b-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="6276b-116">**IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="6276b-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="6276b-117">Proporciona un método para cifrar los datos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6276b-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="6276b-118">**IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="6276b-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="6276b-119">Cifra los datos de bloques no contiguos.</span><span class="sxs-lookup"><span data-stu-id="6276b-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="6276b-120">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="6276b-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="6276b-121">Extensión de la interfaz **IMFMediaEventGenerator** que proporciona un método para cancelar las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="6276b-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="6276b-122">**IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="6276b-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="6276b-123">Habilita la recuperación de información de estado avanzada sobre el progreso de la individualización.</span><span class="sxs-lookup"><span data-stu-id="6276b-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="6276b-124">**IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="6276b-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="6276b-125">Representa una o más licencias en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="6276b-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="6276b-126">**IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="6276b-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="6276b-127">Habilita la recuperación de información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="6276b-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="6276b-128">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="6276b-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="6276b-129">Habilita las operaciones de administración para el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="6276b-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="6276b-130">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="6276b-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="6276b-131">Proporciona opciones de administración adicionales para el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="6276b-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="6276b-132">**IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="6276b-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="6276b-133">Permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="6276b-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="6276b-134">**IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="6276b-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="6276b-135">Proporciona los métodos necesarios para crear una aplicación DRM de Microsoft Windows Media para el receptor de dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="6276b-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="6276b-136">**IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="6276b-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="6276b-137">Proporciona los métodos necesarios para crear una aplicación DRM de Microsoft Windows Media para el transmisor de dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="6276b-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="6276b-138">**IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="6276b-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="6276b-139">Proporciona métodos que permiten la adquisición de licencias con la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="6276b-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="6276b-140">**IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="6276b-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="6276b-141">Crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6276b-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="6276b-142">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="6276b-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="6276b-143">Administra varios procesos relacionados con la seguridad para el equipo cliente y el subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="6276b-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="6276b-144">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="6276b-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="6276b-145">Administra la revocación y renovación de componentes.</span><span class="sxs-lookup"><span data-stu-id="6276b-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="6276b-146">**IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="6276b-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="6276b-147">Habilita el cifrado y descifrado de los búferes.</span><span class="sxs-lookup"><span data-stu-id="6276b-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="6276b-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6276b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6276b-149">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="6276b-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




