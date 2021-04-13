---
title: Realización de una individualización DRM
description: Realización de una individualización DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, individualización de DRM
- SDK de Windows Media Format, individualización
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), individualización
- DRM (administración de derechos digitales), individualización
- Administración de derechos digitales (DRM), individualización de DRM
- DRM (administración de derechos digitales), individualización de DRM
- API extendidas del cliente DRM, individualización
- API extendidas de cliente, individualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357531"
---
# <a name="performing-drm-individualization"></a>Realización de una individualización DRM

La individualización es el proceso de actualizar el componente DRM en el equipo cliente, cifrarlo y hacerlo único. Cuando se crea un equipo, el componente DRM está asociado al equipo y no podrá descodificar el contenido en ningún otro equipo. Las API extendidas del cliente DRM de Windows Media ofrecen compatibilidad para la individualización del componente DRM en los equipos cliente.

La individualización se realiza llamando al método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) . Puede llamar a **PerformSecurityUpdate** para que se pueda individualizar solo si la versión del servidor es más reciente que la instalada en el equipo cliente, o puede forzar la individualización sin tener en cuenta las versiones de seguridad relativas. La marca para la individualización necesaria es la seguridad de WMDRM que \_ \_ realiza \_ indiv. La marca para la individualización forzada es la seguridad de WMDRM y \_ \_ \_ forzar \_ indiv.

**PerformSecurityUpdate** es una llamada asincrónica. Se devolverá rápidamente y después generará eventos para proporcionar información de estado sobre el proceso de individualización. La mayoría de los eventos generados serán eventos **MEWMDRMIndividualizationProgress** y cada uno tiene una interfaz [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociada. Para obtener la interfaz de estado, debe llamar a **IMFMediaEvent:: GetValue** para recuperar un puntero **IUnknown** que esté en el mismo objeto y, a continuación, consultarlo para **IWMDRMIndividualizationStatus**.

Puede obtener datos de una estructura [**de \_ \_ Estado**](drmwm-individualize-status.md) de la función de usuario de WM llamando a [**IWMDRMIndividualizeStatus:: getStatus**](iwmdrmindividualizationstatus-getstatus.md). Cada evento que se genera tiene su propio objeto con estado, por lo que debe seguir el proceso de obtención del valor de evento y la consulta de la interfaz de estado cada vez.

En función del tamaño de la descarga, puede haber docenas o cientos de eventos **MEWMDRMIndividualizationProgress** . Cuando finaliza el proceso de individualización, se genera un evento **MEWMDRMIndividualizationCompleted** .

Cuando se completa la individualización, los únicos objetos existentes que reflejen el nuevo estado de forma individual son los que heredan de [**IWMDRMSecurity**](iwmdrmsecurity.md). No se actualizarán todos los demás objetos existentes. Debe liberar y volver a crear los demás objetos para que reflejen el nuevo estado de forma individual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> <dt>

[**Usar el modelo de eventos Media Foundation**](using-the-media-foundation-model.md)
</dt> <dt>

[Prácticas recomendadas para la individualización de DRM de Windows Media](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




