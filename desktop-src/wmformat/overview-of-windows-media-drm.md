---
title: Información general sobre drm Windows multimedia
description: Información general sobre drm Windows multimedia
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, licencias para DRM
- administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales),acerca de
- administración de derechos digitales (DRM), empaquetado Windows archivos multimedia
- DRM (administración de derechos digitales), empaquetado Windows archivos multimedia
- administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), lectura de archivos protegidos
- DRM (administración de derechos digitales), lectura de archivos protegidos
- Formato de sistemas avanzados (ASF), administración de derechos digitales (DRM)
- ASF (formato de sistemas avanzados), administración de derechos digitales (DRM)
- licenses,DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467076"
---
# <a name="overview-of-windows-media-drm"></a>Información general sobre drm Windows multimedia

Windows Media Digital Rights Management (DRM) es un sistema para proteger el contenido de Windows Media para que los usuarios no autorizados no puedan acceder a él. Hay tres fases en el ciclo básico de DRM: empaquetado, licencias y lectura.

## <a name="packaging-windows-media-files"></a>Empaquetado de Windows archivos multimedia

Windows DRM multimedia está diseñado para funcionar con Windows multimedia. Un archivo Windows Media es un archivo que se ajusta a la especificación del formato de sistemas avanzados (ASF) y solo contiene audio y vídeo que se comprimió mediante los códecs de audio y vídeo multimedia de Windows.

Cuando se empaqueta un archivo ASF, se agrega una sección específica de DRM al encabezado. El encabezado DRM contiene un identificador de clave, que identifica el contenido para los fines de licencia, y una dirección URL de adquisición de licencias, que es la dirección de una página web que puede emitir licencias para leer el contenido protegido. Hay mucha más información que se puede colocar en el encabezado DRM, pero es opcional. El encabezado DRM está firmado para que se pueda comprobar el empaquetador.

El contenido del archivo ASF se cifra durante el proceso de empaquetado. Sin embargo, la siguiente información del archivo empaquetado está disponible incluso para los clientes que no tienen una licencia:

-   Metadatos que se almacenan en el encabezado ASF.
-   Algunos metadatos que se almacenan en el encabezado DRM (por ejemplo, siempre puede obtener la dirección URL de adquisición de licencias).

## <a name="licensing-protected-files"></a>Licencias de archivos protegidos

Para que se lea un archivo empaquetado, se debe emitir una licencia al equipo cliente. Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos. A menudo, se emite una licencia para un archivo protegido en respuesta al usuario que intenta realizar alguna operación en el archivo. Sin embargo, también es posible que un emisor de licencias entregue licencias a un cliente antes de que se solicite explícitamente. Para obtener más información sobre las licencias, vea [Licencias](licenses.md).

## <a name="reading-data-from-protected-files"></a>Lectura de datos de archivos protegidos

Cuando un usuario intenta realizar una operación en un archivo protegido (reproducir, grabar en CD, copiar en un dispositivo, entre otros), la aplicación debe buscar licencias para el contenido en el equipo cliente. Si existe una licencia válida en el equipo cliente, la operación puede continuar. Si no hay una licencia para el contenido o si ninguna licencia para el contenido que está en el equipo cliente permite la acción solicitada, se debe adquirir una licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las API extendidas Windows de cliente DRM multimedia**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




