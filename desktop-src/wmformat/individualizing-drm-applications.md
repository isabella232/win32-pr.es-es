---
title: Individualización de aplicaciones DRM
description: Individualización de aplicaciones DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows SDK de formato multimedia, individualización de aplicaciones DRM
- Windows SDK de formato multimedia, individualización de aplicaciones
- Formato de sistemas avanzados (ASF), individualización de aplicaciones DRM
- ASF (formato de sistemas avanzados), individualización de aplicaciones DRM
- Formato de sistemas avanzados (ASF), individualización de aplicaciones
- ASF (formato de sistemas avanzados), individualización de aplicaciones
- administración de derechos digitales (DRM), individualización de aplicaciones
- DRM (administración de derechos digitales), individualización de aplicaciones
- administración de derechos digitales (DRM), individualización de aplicaciones
- DRM (administración de derechos digitales), individualización de aplicaciones
- individualización de aplicaciones
- individualización de aplicaciones DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c57b6f884e2304508243180cc536899f991b1baab6f7f540f04f12fb805d6f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809025"
---
# <a name="individualizing-drm-applications"></a>Individualización de aplicaciones DRM

Para aumentar la seguridad, el componente DRM de las aplicaciones se *puede individualizar.* Una aplicación individualizada es aquella que ha recibido una actualización de sus componentes DRM que la diferencia de todas las demás copias de la misma aplicación. Los propietarios de contenido pueden requerir que sus archivos protegidos se re reproducen solo en una aplicación que se ha individualizado.

El proceso de individualización se inicia cuando la aplicación se pone en contacto con Microsoft Individualization Service, que luego instala una actualización de seguridad en el equipo del usuario. Dado que el servicio de individualización controla la información del usuario, debe mostrar la directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft: <https://privacy.microsoft.com/privacystatement> .

La individualización se puede realizar de maneras diferentes. Por ejemplo, la individualización puede tener lugar cuando un usuario reproduce un archivo protegido. La solicitud de licencia se envía a [*Windows Servicio*](wmformat-glossary.md)de licencias multimedia , que inspecciona el certificado de la aplicación que solicita la [*licencia*](wmformat-glossary.md). Si el componente DRM de la aplicación no se ha individualizado, Windows Media License Service rechaza la emisión de la licencia, ya que es la directiva de Windows Media License Service emitir licencias solo a reproductores individualizados. A continuación, la aplicación puede notificar al usuario que la aplicación debe actualizarse. Si el usuario acepta, se proporciona una actualización de seguridad para individualizar el componente DRM de la aplicación.

Para mejorar la experiencia del usuario, puede iniciar el proceso de individualización como un paso de actualización de seguridad durante la instalación. a continuación, el usuario no se interrumpe para obtener una actualización de seguridad al intentar reproducir un archivo protegido. También puede fomentar activamente la individualización agregando **un** botón o un comando de menú Actualización de seguridad a la aplicación.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




