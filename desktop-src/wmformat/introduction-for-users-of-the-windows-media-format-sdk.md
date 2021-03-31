---
title: Introducción para los usuarios del SDK de Windows Media Format
description: Introducción para los usuarios del SDK de Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- API extendidas del cliente DRM, acerca de
- API extendidas de cliente, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418747"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Introducción para los usuarios del SDK de Windows Media Format

Gran parte de la funcionalidad proporcionada por las API extendidas del cliente DRM de Windows Media es la misma que la funcionalidad proporcionada por los objetos del SDK de Windows Media Format. El SDK de Windows Media Format proporciona a los desarrolladores los objetos necesarios para crear, obtener acceso y manipular archivos multimedia que usan la estructura de archivos Advanced Systems Format (ASF). Como Windows Media DRM está diseñado para proteger los archivos ASF, se incluyó la funcionalidad DRM del lado cliente en el SDK de Windows Media Format.

Las API extendidas del cliente DRM de Windows Media se publican junto con la plataforma multimedia digital de última generación de Microsoft, el SDK de Microsoft Media Foundation. Media Foundation incluirá la funcionalidad de ASF que se superpone a algunas de las características del SDK de Windows Media Format. Dado que ahora hay dos SDK de Microsoft que manipulan archivos ASF, la funcionalidad DRM del lado cliente se separa del SDK de Windows Media Format en las API extendidas del cliente DRM de Windows Media. Se puede tener acceso a estas API a través de los usuarios de Windows Media Format SDK y del SDK de Media Foundation. En la actualidad, estas API se incluyen como parte del paquete de instalación del SDK de Windows Media Format y se documentan como parte del SDK de Windows Media Format. Sin embargo, las API extendidas del cliente DRM de Windows Media se implementan en su propia biblioteca y tienen su propio archivo de encabezado. Después de instalar el SDK de Windows Media Format, estas API se pueden usar una por su cuenta, sin incluir ningún encabezado o biblioteca de Windows Media Format SDK en la aplicación.

Si desarrolla aplicaciones que usan el SDK de Windows Media Format, debe decidir si va a usar la funcionalidad DRM que proporciona el SDK o si desea usar las API extendidas del cliente DRM de Windows Media. Aunque muchas de las características de estos dos SDK son muy similares, las API extendidas del cliente DRM de Windows Media ofrecen las siguientes características que no están disponibles para los usuarios de las rutinas DRM anteriores:

-   Capacidad de importar contenido protegido por un sistema de administración de derechos de terceros.
-   Capacidad de exportar contenido protegido por DRM de Windows Media a un sistema de administración de derechos de terceros.
-   Enumeración directa de licencias en el almacén de licencias.
-   Consultas de derechos simples y agregadas basadas en el identificador de clave (no es necesario cargar el archivo multimedia).
-   Capacidad de renovar componentes revocados mediante la interfaz de Media Foundation estándar, **IMFContentEnabler**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las API extendidas del cliente DRM de Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




