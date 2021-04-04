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
# <a name="using-the-media-foundation-event-model"></a>Usar el modelo de eventos Media Foundation

Los métodos asincrónicos que admiten las API extendidas del cliente DRM de Windows Media usan el mismo modelo de eventos que usa el SDK de Media Foundation. Cada objeto que admite métodos asincrónicos implementa la interfaz [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , que se puede usar para recuperar un evento cuando se completa una operación asincrónica.

La interfaz **IWMDRMEventGenerator** se hereda de la interfaz **IMFMediaEventGenerator** , que se documenta en la documentación del SDK de Media Foundation.

En el código de ejemplo del [ejemplo de individualización de DRM](drm-individualization-example.md) se usa el método **IMFMediaEventGenerator:: GetEvent** para recuperar los eventos de la cola de uno en uno. El uso de **GetEvent** es más sencillo que usar **IMFMediaEventGenerator:: BeginGetEvent** y **IMFMediaEventGenerator:: EndGetEvent** con una devolución de llamada, lo que hace que los ejemplos de código sean más fáciles de entender. Tanto si usa **GetEvent** en el código como si implementa **IMFAsyncCallback** y usa **BeginGetEvent** y **EndGetEvent**, la lógica para controlar el evento una vez recibido es la misma.

Algunos de los métodos asincrónicos generan eventos que contienen referencias a objetos que se pueden usar para obtener información de estado más detallada. En estos casos, el evento generado tiene un puntero **IUnknown** como su valor, que se puede consultar para recuperar la interfaz de estado. En la lista siguiente se resumen las relaciones entre las llamadas asincrónicas, los eventos generados y otras interfaces.

-   El método [**IWMDRMLicenseManagement:: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) genera eventos **MEWMDRMLicenseBackupProgress** con las interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.
-   El método [**IWMDRMLicenseManagement:: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) genera eventos **MEWMDRMLicenseRestoreProgress** con las interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) asociadas.
-   El método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , cuando se usa para realizar la individualización, genera eventos **MEWMDRMIndividualizationProgress** con las interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociadas.
-   El método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , cuando se usa para preparar los datos para la adquisición de licencias no silenciosas, genera un evento **MEWMDRMLicenseAcquisitionCompleted** con una interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) asociada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Introducción**](drm-getting-started.md)
</dt> <dt>

[Documentación del SDK de Media Foundation](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




