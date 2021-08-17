---
title: Individualización de DRM
description: Individualización de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows SDK de formato multimedia, individualización de DRM
- digital rights management (DRM), individualización
- DRM (administración de derechos digitales), individualización
- individualización de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16704c968002ee9d9d9cd9a47bf71dd315c2c599848b2ea18b23408ec7a0507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848697"
---
# <a name="drm-individualization"></a>Individualización de DRM

Los propietarios de contenido protegido pueden requerir que los usuarios actualicen algunos de los componentes de administración de derechos digitales (DRM) incluidos en el SDK de formato multimedia de Windows antes de acceder a su contenido. Si un usuario acepta la actualización, se descargará una versión individualizada de un archivo de seguridad (una única para su equipo) desde un sitio web de Microsoft. Si el usuario rechaza la actualización, no podrá acceder al contenido; sin embargo, seguirán siendo capaces de acceder al contenido no protegido y al contenido protegido que no requiera la actualización. La realización de una actualización de seguridad ayuda a aumentar el nivel de protección que ofrece DRM.

La individualización se puede realizar en el momento de la instalación o cuando una aplicación encuentra por primera vez un archivo ASF protegido que lo requiere. Dado que este proceso modifica los componentes del sistema de un usuario, la aplicación debe notificar al usuario y obtener su consentimiento informado antes de realizar la actualización. Microsoft Reproductor de Windows Media, por ejemplo, muestra un cuadro de diálogo con el texto siguiente:

**Actualización de seguridad necesaria**

**El propietario del contenido protegido al que está intentando acceder requiere que primero actualice algunos de los componentes de Administración de derechos digitales (DRM) de Microsoft en el equipo.**

**Haga clic en Aceptar para actualizar los componentes de DRM.**

**Detalles:**

**Al hacer clic en Aceptar, se envían un identificador único y un archivo de seguridad DRM a un servicio de Microsoft en Internet. El archivo se reemplaza por una versión personalizada que contiene el identificador único. Esto aumenta el nivel de protección proporcionado por DRM.**

Cualquier aplicación que admita la individualización debe usar la misma redacción o similar. Para obtener más información sobre la directiva de privacidad de Microsoft, consulte la sección [Declaración de](privacy-statement.md) privacidad de esta documentación.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Individualización de aplicaciones DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




