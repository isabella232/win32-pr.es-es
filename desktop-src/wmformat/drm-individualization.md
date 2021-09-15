---
title: Individualización de DRM
description: Individualización de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows SDK de formato multimedia, individualización de DRM
- administración de derechos digitales (DRM),individualización
- DRM (administración de derechos digitales), individualización
- individualización de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247382"
---
# <a name="drm-individualization"></a>Individualización de DRM

Los propietarios de contenido protegido pueden requerir que los usuarios actualicen algunos de los componentes de administración de derechos digitales (DRM) incluidos en el SDK de formato multimedia de Windows antes de acceder a su contenido. Si un usuario acepta la actualización, se descargará una versión individualizada de un archivo de seguridad (una única para su equipo) desde un sitio web de Microsoft. Si el usuario rechaza la actualización, no podrá acceder al contenido; sin embargo, seguirán siendo capaces de acceder al contenido no protegido y al contenido protegido que no requiere la actualización. La realización de una actualización de seguridad ayuda a aumentar el nivel de protección que ofrece DRM.

La individualización se puede realizar en el momento de la instalación o cuando una aplicación encuentra por primera vez un archivo ASF protegido que lo requiere. Dado que este proceso modifica los componentes del sistema de un usuario, la aplicación debe notificar al usuario y obtener su consentimiento informado antes de realizar la actualización. Microsoft Reproductor de Windows Media, por ejemplo, muestra un cuadro de diálogo con el texto siguiente:

**Actualización de seguridad necesaria**

**El propietario del contenido protegido al que intenta acceder requiere que primero actualice algunos de los componentes de Administración de derechos digitales (DRM) de Microsoft en el equipo.**

**Haga clic en Aceptar para actualizar los componentes de DRM.**

**Detalles:**

**Al hacer clic en Aceptar, se envían un identificador único y un archivo de seguridad DRM a un servicio de Microsoft en Internet. El archivo se reemplaza por una versión personalizada que contiene el identificador único. Esto aumenta el nivel de protección proporcionado por DRM.**

Cualquier aplicación que admita la individualización debe usar la misma palabra o similar. Para obtener más información sobre la directiva de privacidad de Microsoft, consulte la sección [Declaración de](privacy-statement.md) privacidad de esta documentación.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Individualización de aplicaciones DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




