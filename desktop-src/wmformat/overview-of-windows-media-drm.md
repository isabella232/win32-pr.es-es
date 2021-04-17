---
title: Información general de DRM de Windows Media
description: Información general de DRM de Windows Media
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales), acerca de
- Administración de derechos digitales (DRM), empaquetar archivos de Windows Media
- DRM (administración de derechos digitales), empaquetar archivos de Windows Media
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), lectura de archivos protegidos
- DRM (administración de derechos digitales), leer archivos protegidos
- Advanced Systems Format (ASF), administración de derechos digitales (DRM)
- ASF (formato de sistemas avanzados), administración de derechos digitales (DRM)
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704579"
---
# <a name="overview-of-windows-media-drm"></a>Información general de DRM de Windows Media

Windows Media Digital Rights Management (DRM) es un sistema para proteger el contenido de los archivos de Windows Media para que los usuarios no autorizados no puedan tener acceso a él. Hay tres fases en el ciclo básico de DRM: empaquetado, licencias y lectura.

## <a name="packaging-windows-media-files"></a>Empaquetar archivos de Windows Media

Windows Media DRM está diseñado para trabajar con archivos de Windows Media. Un archivo de Windows Media es un archivo que se ajusta a la especificación de Advanced Systems Format (ASF) y que solo contiene audio y vídeo comprimidos mediante los códecs de Windows Media Audio y vídeo.

Cuando se empaqueta un archivo ASF, se agrega una sección específica de DRM al encabezado. El encabezado DRM contiene un identificador de clave que identifica el contenido con fines de licencia y una dirección URL de adquisición de licencias, que es la dirección de una página web que puede emitir licencias para leer el contenido protegido. Hay mucha más información que se puede colocar en el encabezado DRM, pero es opcional. El encabezado DRM está firmado para que se pueda comprobar el empaquetador.

El contenido del archivo ASF se cifra durante el proceso de empaquetado. Sin embargo, la siguiente información en el archivo empaquetado está disponible incluso para los clientes que no tienen una licencia:

-   Metadatos que se almacenan en el encabezado ASF.
-   Algunos metadatos que se almacenan en el encabezado DRM (por ejemplo, siempre puede obtener la dirección URL de adquisición de licencias).

## <a name="licensing-protected-files"></a>Archivos protegidos con licencias

Para que se pueda leer un archivo empaquetado, debe emitirse una licencia para el equipo cliente. Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos. La mayoría de las veces, se emite una licencia para un archivo protegido en respuesta al usuario que intenta realizar alguna operación en el archivo. Sin embargo, también es posible que un emisor de licencias entregue licencias a un cliente antes de que se solicite explícitamente. Para obtener más información sobre las licencias, consulte [licencias](licenses.md).

## <a name="reading-data-from-protected-files"></a>Leer datos de archivos protegidos

Cuando un usuario intenta realizar una operación en un archivo protegido (reproducir, grabar en CD, copiar en un dispositivo, etc.), la aplicación debe comprobar si hay licencias para el contenido en el equipo cliente. Si existe una licencia válida en el equipo cliente, la operación puede continuar. Si no hay una licencia para el contenido, o si ninguna licencia para el contenido que se encuentra en el equipo cliente permite la acción solicitada, se debe adquirir una licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las API extendidas del cliente DRM de Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




