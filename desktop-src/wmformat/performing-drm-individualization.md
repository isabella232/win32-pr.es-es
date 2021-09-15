---
title: Realización de la individualización de DRM
description: Realización de la individualización de DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows SDK de formato multimedia, API extendidas de cliente DRM
- Windows SDK de formato multimedia, API extendidas de cliente
- Windows SDK de formato multimedia, API extendidas
- Windows SDK de formato multimedia, API
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, individualización de DRM
- Windows SDK de formato multimedia, individualización
- administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- digital rights management (DRM), individualización
- DRM (administración de derechos digitales), individualización
- administración de derechos digitales (DRM), individualización de DRM
- DRM (administración de derechos digitales), individualización de DRM
- API extendidas de cliente DRM, individualización
- API extendidas de cliente, individualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467073"
---
# <a name="performing-drm-individualization"></a>Realización de la individualización de DRM

La individualización es el proceso de actualizar el componente DRM en el equipo cliente, cifrarlo y hacer que sea único. Cuando un equipo se individualiza, el componente DRM está asociado al equipo y no podrá descodificar contenido en ningún otro equipo. Las API extendidas Windows de cliente DRM multimedia proporcionan compatibilidad para individualizar el componente DRM en los equipos cliente.

La individualización se realiza mediante una llamada [**al método IWMDRMSecurity::P erformSecurityUpdate.**](iwmdrmsecurity-performsecurityupdate.md) Puede llamar a **PerformSecurityUpdate** para que se individualice solo si la versión del servidor es más reciente que la instalada en el equipo cliente, o puede forzar la individualización sin tener en cuenta las versiones de seguridad relativas. La marca para la individualización según sea necesario es WMDRM \_ SECURITY \_ PERFORM \_ INDIV. La marca para la individualización forzada es WMDRM \_ SECURITY \_ PERFORM FORCE \_ \_ INDIV.

**PerformSecurityUpdate es** una llamada asincrónica. Se devolverá rápidamente y, a continuación, generará eventos para proporcionar información de estado sobre el proceso de individualización. La mayoría de los eventos generados serán eventos **MEWMDRMIndividualizationProgress** y cada uno tiene una interfaz [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociada. Para obtener la interfaz de estado, debe llamar a **IMFMediaEvent::GetValue** para recuperar un **puntero IUnknown** que se encuentra en el mismo objeto y, a continuación, consultarlo para **IWMDRMIndividualizationStatus**.

Puede obtener datos para una estructura [**WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) llamando a [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Cada evento que se genera tiene su propio objeto con estado, por lo que debe seguir el proceso de obtener el valor del evento y consultar la interfaz de estado cada vez.

Según el tamaño de la descarga, puede haber docenas o cientos de eventos **MEWMDRMIndividualizationProgress.** Cuando finaliza el proceso de individualización, se genera un evento **MEWMDRMIndividualizationCompleted.**

Cuando se completa la individualización, los únicos objetos existentes que reflejarán el nuevo estado individualizado son los que heredan de [**IWMDRMSecurity**](iwmdrmsecurity.md). No se actualizarán todos los demás objetos existentes. Debe liberar y volver a crear cualquier otro objeto para que refleje el nuevo estado individualizado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> <dt>

[**Uso del modelo Media Foundation eventos**](using-the-media-foundation-model.md)
</dt> <dt>

[Windows Procedimientos recomendados de individualización de DRM multimedia](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




