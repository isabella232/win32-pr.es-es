---
title: Copia de seguridad y restauración de licencias DRM
description: Copia de seguridad y restauración de licencias DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows SDK de formato multimedia, copia de seguridad de licencias DRM
- Windows SDK de formato multimedia, restaurar licencias DRM
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, licencias para DRM
- Windows SDK de formato multimedia, característica de restauración de copia de seguridad
- Windows SDK de formato multimedia, Servicio de administración de licencias
- Windows SDK de formato multimedia, detección de fraudes
- administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- administración de derechos digitales (DRM),licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), característica de restauración de copia de seguridad
- DRM (administración de derechos digitales), característica de restauración de copia de seguridad
- administración de derechos digitales (DRM),Servicio de administración de licencias
- DRM (administración de derechos digitales),Servicio de administración de licencias
- administración de derechos digitales (DRM), detección de fraudes
- DRM (administración de derechos digitales), detección de fraudes
- copia de seguridad de licencias DRM
- restaurar licencias DRM
- licenses,DRM
- licencias, copia de seguridad de DRM
- licencias, restaurar DRM
- Característica de restauración de copia de seguridad
- Servicio de administración de licencias
- detección de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019163a42312b14b7d7b7e15cea68be1996a976e42b31491f62486a43d37b8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028153"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Copia de seguridad y restauración de licencias DRM

Con la característica Restaurar copia de seguridad, los usuarios pueden realizar copias de seguridad y restaurar [*licencias*](wmformat-glossary.md) en el mismo equipo o en otros equipos. Esta característica permite a los usuarios transferir licencias a un nuevo equipo o volver al mismo equipo (por ejemplo, después de volver a formatear el disco duro). Además, los usuarios pueden reproducir archivos ASF protegidos en más de un equipo.

Para fomentar el uso legítimo de una licencia, una directiva de detección de fraudes restringe el número de veces que se puede restaurar una licencia. Microsoft proporciona un servicio que realiza un seguimiento del número de equipos en los que se ha restaurado una licencia. Si se alcanza un límite, el usuario no puede restaurar la licencia.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Permitir o no permitir el derecho de copia de seguridad y restauración

La característica De restauración de copia de seguridad solo funciona para las licencias para las que se da el derecho copia de seguridad y restauración. Si los propietarios de contenido o los emisores de licencias no desean esta característica, o si emiten licencias que contienen un estado seguro (por ejemplo, operaciones con recuento o tiempo limitado), pueden no permitir este derecho.

Cuando no se puede restaurar una licencia porque un usuario no tiene el derecho, [*se*](wmformat-glossary.md) pasa un identificador de clave a la aplicación. Como mínimo, se debe notificar al usuario que no se pudo realizar una copia de seguridad de algunas licencias, aunque el usuario no sabe a qué licencias hace referencia este mensaje. Si conoce el identificador de clave de los archivos protegidos disponibles, puede desarrollar una solución más sólida para informar al usuario.

Por ejemplo, se podría desarrollar un reproductor para una etiqueta de registro que proporciona canciones protegidas en Internet. Se puede realizar un seguimiento de estas canciones y sus principales iDs en una base de datos. Si no se pudo realizar una copia de seguridad de algunas licencias, la aplicación player podría usar el identificador de clave para consultar el nombre de las canciones en la base de datos y, a continuación, informar al usuario para qué canciones no se puede realizar una copia de seguridad de las licencias. O bien, se podría crear una biblioteca de música para cada usuario localmente y el identificador de clave podría usarse para recuperar más información sobre las licencias de las que no se pudo realizar una copia de seguridad.

## <a name="the-license-management-service"></a>El servicio de administración de licencias

Cuando se implementa la característica de restauración de copia de seguridad, un servicio de administración de licencias hospedado por Microsoft administra la restauración de licencias.

En primer lugar, los usuarios copian las licencias de la aplicación, por ejemplo, eligiendo una opción de menú. Todas las licencias del equipo se copian en una ubicación especificada, como un disquete. A continuación, los usuarios restauran licencias mediante la aplicación, por ejemplo, eligiendo una opción de menú y especificando su ubicación de copia de seguridad.

En este momento, el usuario debe estar conectado a Internet; Se envía una solicitud de la aplicación al servicio de administración de licencias. Si el equipo del que se ha realizado la copia de seguridad de la licencia es diferente del equipo original (o se ha vuelto a formatear el equipo original), el Servicio de administración de licencias emite una nueva licencia para el nuevo equipo. De lo contrario, se vuelve a emitir la licencia que se emitió anteriormente para ese equipo.

Dado que el servicio de administración de licencias recupera información del usuario, debe mostrar la directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio [web de Microsoft](https://www.microsoft.com/licensing/default).

> [!Note]  
> Cuando un usuario final restaura una licencia en un equipo diferente y la licencia requiere individualización, el usuario final debe autorizar la actualización de los componentes drm. Debe implementar un proceso en la aplicación de reproductor para admitir esta característica.

 

## <a name="detecting-fraud"></a>Detección de fraudes

El usuario puede restaurar una licencia un número limitado de veces. Cada vez que se restaura una licencia, el Servicio de administración de licencias realiza un seguimiento de ella e incrementa el recuento de esa licencia en una. Al restaurar una licencia en un equipo en el que se ha restaurado la licencia anteriormente (por ejemplo, el equipo desde el que se ha realizado la copia de seguridad de la licencia), el recuento no aumenta. Se considera que un equipo es diferente si tiene un nuevo sistema operativo o si se ha instalado de nuevo el sistema operativo.

De acuerdo con la directiva de detección de fraudes de Microsoft, cuando una licencia se ha restaurado un número determinado de veces, la aplicación recibe una dirección URL de los componentes de DRM y es responsable de abrir un explorador y mostrar la página web, lo que indica que el contrato de licencia podría haber sido infringido. El usuario debe ponerse en contacto con el distribuidor de licencias, que debe determinar si la solicitud es válida.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Copia de seguridad y restauración de licencias**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




