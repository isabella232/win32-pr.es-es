---
title: Usar el modelo de eventos Media Foundation
description: Usar el modelo de eventos Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK, DRM Media Foundation modelo de eventos
- SDK de Windows Media Format, Media Foundation modelo de eventos
- SDK de Windows Media Format, modelo de eventos de DRM
- Administración de derechos digitales (DRM), Media Foundation modelo de eventos
- DRM (administración de derechos digitales), Media Foundation modelo de eventos
- Administración de derechos digitales (DRM), modelo de eventos
- DRM (administración de derechos digitales), modelo de eventos
- Administración de derechos digitales (DRM), interfaz IWMDRMEventGenerator
- DRM (administración de derechos digitales), interfaz IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077386"
---
# <a name="using-the-media-foundation-event-model"></a><span data-ttu-id="12c4a-114">Usar el modelo de eventos Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12c4a-114">Using the Media Foundation Event Model</span></span>

<span data-ttu-id="12c4a-115">Los métodos asincrónicos que admiten las API extendidas del cliente DRM de Windows Media usan el mismo modelo de eventos que usa el SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="12c4a-115">The asynchronous methods supported by the Windows Media DRM Client Extended APIs use the same event model that is used by the Media Foundation SDK.</span></span> <span data-ttu-id="12c4a-116">Cada objeto que admite métodos asincrónicos implementa la interfaz [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , que se puede usar para recuperar un evento cuando se completa una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="12c4a-116">Each object that supports asynchronous methods implements the [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) interface, which can be used to retrieve an event when an asynchronous operation is complete.</span></span>

<span data-ttu-id="12c4a-117">La interfaz **IWMDRMEventGenerator** se hereda de la interfaz **IMFMediaEventGenerator** , que se documenta en la documentación del SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="12c4a-117">The **IWMDRMEventGenerator** interface inherits from the **IMFMediaEventGenerator** interface, which is documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="12c4a-118">En el código de ejemplo del [ejemplo de individualización de DRM](drm-individualization-example.md) se usa el método **IMFMediaEventGenerator:: GetEvent** para recuperar los eventos de la cola de uno en uno.</span><span class="sxs-lookup"><span data-stu-id="12c4a-118">The example code in the [DRM Individualization Example](drm-individualization-example.md) uses the **IMFMediaEventGenerator::GetEvent** method to retrieve events from the queue one at a time.</span></span> <span data-ttu-id="12c4a-119">El uso de **GetEvent** es más sencillo que usar **IMFMediaEventGenerator:: BeginGetEvent** y **IMFMediaEventGenerator:: EndGetEvent** con una devolución de llamada, lo que hace que los ejemplos de código sean más fáciles de entender.</span><span class="sxs-lookup"><span data-stu-id="12c4a-119">Using **GetEvent** is more straightforward than using **IMFMediaEventGenerator::BeginGetEvent** and **IMFMediaEventGenerator::EndGetEvent** with a callback, which makes the code examples easier to understand.</span></span> <span data-ttu-id="12c4a-120">Tanto si usa **GetEvent** en el código como si implementa **IMFAsyncCallback** y usa **BeginGetEvent** y **EndGetEvent**, la lógica para controlar el evento una vez recibido es la misma.</span><span class="sxs-lookup"><span data-stu-id="12c4a-120">Whether you use **GetEvent** in your code or implement **IMFAsyncCallback** and use **BeginGetEvent** and **EndGetEvent**, the logic to handle the event after it has been received is the same.</span></span>

<span data-ttu-id="12c4a-121">Algunos de los métodos asincrónicos generan eventos que contienen referencias a objetos que se pueden usar para obtener información de estado más detallada.</span><span class="sxs-lookup"><span data-stu-id="12c4a-121">Several of the asynchronous methods generate events that contain references to objects that can be used to obtain more detailed status information.</span></span> <span data-ttu-id="12c4a-122">En estos casos, el evento generado tiene un puntero **IUnknown** como su valor, que se puede consultar para recuperar la interfaz de estado.</span><span class="sxs-lookup"><span data-stu-id="12c4a-122">In these cases, the generated event has an **IUnknown** pointer as its value, which can be queried to retrieve the status interface.</span></span> <span data-ttu-id="12c4a-123">En la lista siguiente se resumen las relaciones entre las llamadas asincrónicas, los eventos generados y otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="12c4a-123">The following list summarizes the relationships between asynchronous calls, generated events, and other interfaces.</span></span>

-   <span data-ttu-id="12c4a-124">El método [**IWMDRMLicenseManagement:: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) genera eventos **MEWMDRMLicenseBackupProgress** con las interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.</span><span class="sxs-lookup"><span data-stu-id="12c4a-124">The [**IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method generates **MEWMDRMLicenseBackupProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="12c4a-125">El método [**IWMDRMLicenseManagement:: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) genera eventos **MEWMDRMLicenseRestoreProgress** con las interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.</span><span class="sxs-lookup"><span data-stu-id="12c4a-125">The [**IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) method generates **MEWMDRMLicenseRestoreProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="12c4a-126">El método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , cuando se usa para realizar la individualización, genera eventos **MEWMDRMIndividualizationProgress** con las interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociadas.</span><span class="sxs-lookup"><span data-stu-id="12c4a-126">The [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, when used to perform individualization, generates **MEWMDRMIndividualizationProgress** events with associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interfaces.</span></span>
-   <span data-ttu-id="12c4a-127">El método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , cuando se usa para preparar los datos para la adquisición de licencias no silenciosas, genera un evento **MEWMDRMLicenseAcquisitionCompleted** con una interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="12c4a-127">The [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method, when used to prepare data for non-silent license acquisition, generates an **MEWMDRMLicenseAcquisitionCompleted** event with an associated [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12c4a-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12c4a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12c4a-129">**Ejemplo de individualización de DRM**</span><span class="sxs-lookup"><span data-stu-id="12c4a-129">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="12c4a-130">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="12c4a-130">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="12c4a-131">Documentación del SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12c4a-131">Media Foundation SDK Documentation</span></span>](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




