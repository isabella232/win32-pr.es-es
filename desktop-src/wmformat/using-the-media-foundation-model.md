---
title: Uso del modelo Media Foundation eventos
description: Uso del modelo Media Foundation eventos
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows SDK de formato multimedia, DRM Media Foundation modelo de eventos
- Windows SDK de formato multimedia, Media Foundation modelo de eventos
- Windows SDK de formato multimedia, modelo de eventos DRM
- digital rights management (DRM),Media Foundation de eventos
- DRM (administración de derechos digitales), Media Foundation modelo de eventos
- digital rights management (DRM), modelo de eventos
- DRM (administración de derechos digitales), modelo de eventos
- digital rights management (DRM), interfaz IWMDRMEventGenerator
- DRM (administración de derechos digitales), interfaz IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32c68d1d22c6b3d95c34efb5a919c82ecf5dd3755943e96f2507ae9f3391f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707395"
---
# <a name="using-the-media-foundation-event-model"></a>Uso del modelo Media Foundation eventos

Los métodos asincrónicos admitidos por Windows MEDIA DRM Client Extended API usan el mismo modelo de eventos que usa Media Foundation SDK. Cada objeto que admite métodos asincrónicos implementa la interfaz [**IWMDRMEventGenerator,**](iwmdrmeventgenerator.md) que se puede usar para recuperar un evento cuando se completa una operación asincrónica.

La **interfaz IWMDRMEventGenerator** hereda de la interfaz **IMFMediaEventGenerator,** que se documenta en la documentación Media Foundation SDK.

El código de ejemplo del ejemplo [de individualización de DRM](drm-individualization-example.md) usa el método **IMFMediaEventGenerator::GetEvent** para recuperar eventos de la cola de uno en uno. El uso de **GetEvent** es más sencillo que usar **IMFMediaEventGenerator::BeginGetEvent** y **IMFMediaEventGenerator::EndGetEvent** con una devolución de llamada, lo que hace que los ejemplos de código sean más fáciles de entender. Tanto si usa **GetEvent** en el código como si implementa **IMFAsyncCallback** y usa **BeginGetEvent** y **EndGetEvent,** la lógica para controlar el evento una vez recibido es la misma.

Varios de los métodos asincrónicos generan eventos que contienen referencias a objetos que se pueden usar para obtener información de estado más detallada. En estos casos, el evento generado tiene un puntero **IUnknown** como valor, que se puede consultar para recuperar la interfaz de estado. En la lista siguiente se resumen las relaciones entre llamadas asincrónicas, eventos generados y otras interfaces.

-   El [**método IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) genera eventos **MEWMDRMLicenseBackupProgress** con interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.
-   El [**método IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) genera eventos **MEWMDRMLicenseRestoreProgress** con interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.
-   El [**método IWMDRMSecurity::P erformSecurityUpdate,**](iwmdrmsecurity-performsecurityupdate.md) cuando se usa para realizar la individualización, genera eventos **MEWMDRMIndividualizationProgress** con interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociadas.
-   El [**método IWMDRMLicenseManagement::AcquireLicense,**](iwmdrmlicensemanagement-acquirelicense.md) cuando se usa para preparar datos para la adquisición de licencias no silenciosas, genera un evento **MEWMDRMLicenseAcquisitionCompleted** con una interfaz [**IWMDRMNonSilentLicenseAquisisition**](iwmdrmnonsilentlicenseaquisition.md) asociada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Tareas iniciales**](drm-getting-started.md)
</dt> <dt>

[documentación Media Foundation SDK de Media Foundation](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




