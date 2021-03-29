---
title: Individualización de aplicaciones DRM
description: Individualización de aplicaciones DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- SDK de Windows Media Format, individualización de aplicaciones DRM
- SDK de Windows Media Format, aplicación en persona
- Advanced Systems Format (ASF), individualización de aplicaciones DRM
- ASF (formato de sistemas avanzados), individualización de aplicaciones DRM
- Advanced Systems Format (ASF), aplicación en persona
- ASF (formato de sistemas avanzados), aplicación en persona
- Administración de derechos digitales (DRM), individualización de aplicaciones
- DRM (administración de derechos digitales), individualización de aplicaciones
- Administración de derechos digitales (DRM), aplicación en persona
- DRM (administración de derechos digitales), aplicación en persona
- aplicación en persona
- individualización de aplicaciones DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103995016"
---
# <a name="individualizing-drm-applications"></a>Individualización de aplicaciones DRM

Para aumentar la seguridad, se puede *individualizar* el componente DRM de las aplicaciones. Una aplicación individualizada es aquella que ha recibido una actualización a sus componentes de DRM que la diferencia de todas las demás copias de la misma aplicación. Los propietarios de contenido pueden exigir que sus archivos protegidos se reproduzcan solo en una aplicación que se ha individualizado.

El proceso de individualización se inicia cuando la aplicación se pone en contacto con el servicio de Microsoft individualización y, a continuación, instala una actualización de seguridad en el equipo del usuario. Dado que el servicio de individualización controla la información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft: <https://privacy.microsoft.com/privacystatement> .

La individualización puede realizarse de diferentes maneras. Por ejemplo, la individualización puede tener lugar cuando un usuario reproduce un archivo protegido. La solicitud de licencia se envía al [*servicio de licencias de Windows Media*](wmformat-glossary.md), que inspecciona el certificado de la aplicación que solicita la [*licencia*](wmformat-glossary.md). Si el componente DRM de la aplicación no se ha individualizado, el servicio de licencias de Windows Media rechaza emitir la licencia, ya que es la Directiva del servicio de licencias de Windows Media para emitir licencias solo a reproductores individualizados. A continuación, la aplicación puede notificar al usuario que la aplicación debe actualizarse. Si el usuario acepta, se proporciona una actualización de seguridad para individualizar el componente DRM de la aplicación.

Para mejorar la experiencia del usuario, puede iniciar el proceso de individualización como un paso de actualización de seguridad durante la instalación. no se interrumpe al usuario para obtener una actualización de seguridad al intentar reproducir un archivo protegido. También puede promover activamente la individualización agregando un comando de menú o un botón de **actualización de seguridad** a la aplicación.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




