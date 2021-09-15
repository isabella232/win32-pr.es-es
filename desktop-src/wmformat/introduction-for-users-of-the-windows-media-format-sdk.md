---
title: Introducción a los usuarios del SDK Windows Media Format
description: Introducción a los usuarios del SDK Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows SDK de formato multimedia, API extendidas de cliente DRM
- Windows SDK de formato multimedia, API extendidas de cliente
- Windows SDK de formato multimedia, API extendidas
- Windows SDK de formato multimedia, API
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- API extendidas de cliente DRM, acerca de
- API extendidas de cliente, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572193"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Introducción a los usuarios del SDK Windows Media Format

Gran parte de la funcionalidad proporcionada por las API extendidas del cliente DRM de Windows Media es la misma que la funcionalidad proporcionada por los objetos del SDK Windows Media Format. El SDK Windows Media Format proporciona a los desarrolladores los objetos necesarios para crear, acceder y manipular archivos multimedia que usan la estructura de archivos de formato de sistemas avanzados (ASF). Dado Windows DRM de multimedia está diseñado para proteger los archivos ASF, la funcionalidad DRM del lado cliente se incluyó en el SDK Windows Media Format.

Las API extendidas de Windows Media DRM Client se están lanzando junto con la plataforma de medios digitales de próxima generación de Microsoft, Microsoft Media Foundation SDK. Media Foundation la funcionalidad de ASF que se superpone a algunas de las características del SDK Windows Media Format. Dado que ahora hay dos SDK de Microsoft que manipulan archivos ASF, la funcionalidad DRM del lado cliente se separa del SDK de formato multimedia de Windows en las API extendidas del cliente drm de Windows Media. Los usuarios del SDK de formato multimedia de Windows y el SDK de Media Foundation pueden acceder a estas API. En la actualidad, estas API se incluyen como parte del paquete de instalación del SDK de formato multimedia de Windows y se documentan como parte del SDK Windows Media Format. Sin embargo, Windows API extendidas de cliente DRM multimedia se implementan en su propia biblioteca y tienen su propio archivo de encabezado. Después de instalar el SDK Windows Media Format, estas API se pueden usar propias, sin incluir bibliotecas ni encabezados del SDK de formato multimedia de Windows en la aplicación.

Si desarrolla aplicaciones que usan el SDK de formato multimedia de Windows, debe decidir si desea usar la funcionalidad DRM que proporciona el SDK o usar las API extendidas del cliente DRM de Windows Media. Aunque muchas de las características de estos dos SDK son muy similares, las API extendidas del cliente DRM de Windows Media ofrecen las siguientes características que no están disponibles para los usuarios de las rutinas DRM anteriores:

-   Capacidad de importar contenido protegido por un sistema de administración de derechos de terceros.
-   Capacidad de exportar contenido protegido por Windows DRM multimedia a un sistema de administración de derechos de terceros.
-   Enumeración directa de licencias en el almacén de licencias.
-   Consulta de derechos simples y agregados en función del identificador de clave (no es necesario cargar el archivo multimedia).
-   Capacidad de renovar componentes revocados mediante la interfaz Media Foundation estándar, **IMFContentEnabler**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las API extendidas Windows de cliente DRM multimedia**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




