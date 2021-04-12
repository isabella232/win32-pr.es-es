---
title: Individualización de DRM
description: Individualización de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- SDK de Windows Media Format, individualización de DRM
- Administración de derechos digitales (DRM), individualización
- DRM (administración de derechos digitales), individualización
- individualización de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356890"
---
# <a name="drm-individualization"></a>Individualización de DRM

Los propietarios de contenido protegido pueden requerir a los usuarios que actualicen algunos de los componentes de administración de derechos digitales (DRM) incluidos en el SDK de Windows Media Format antes de tener acceso a su contenido. Si un usuario acepta la actualización, se descargará una versión individual de un archivo de seguridad (una única para su equipo) desde un sitio web de Microsoft. Si el usuario rechaza la actualización, no podrá tener acceso al contenido. sin embargo, todavía podrán acceder al contenido no protegido y al contenido protegido que no requiera la actualización. La realización de una actualización de seguridad ayuda a aumentar el nivel de protección que ofrece DRM.

La individualización se puede realizar en el momento de la instalación o cuando una aplicación encuentra por primera vez un archivo ASF protegido que lo requiere. Dado que este proceso modifica los componentes del sistema de un usuario, la aplicación debe notificar al usuario y obtener su consentimiento informado antes de realizar la actualización. Microsoft Windows Media Player, por ejemplo, muestra un cuadro de diálogo con el siguiente texto:

**Actualización de seguridad necesaria**

**El propietario del contenido protegido al que está intentando obtener acceso requiere que primero actualice algunos de los componentes de administración de derechos digitales (DRM) de Microsoft en el equipo.**

**Haga clic en Aceptar para actualizar los componentes de DRM.**

**Indicaciones**

**Al hacer clic en aceptar, se envían un identificador único y un archivo de seguridad DRM a un servicio de Microsoft en Internet. El archivo se reemplaza por una versión personalizada que contiene el identificador único. Esto aumenta el nivel de protección proporcionado por DRM.**

Cualquier aplicación que admita la individualización debe utilizar el mismo texto u otro similar. Para obtener más información sobre la Directiva de privacidad de Microsoft, consulte la sección [declaración de privacidad](privacy-statement.md) de esta documentación.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Individualización de aplicaciones DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




