---
title: Copia de seguridad y restauración de licencias de DRM
description: Copia de seguridad y restauración de licencias de DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- SDK de Windows Media Format, copia de seguridad de licencias de DRM
- SDK de Windows Media Format, restaurar licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, característica de restauración de copia de seguridad
- SDK de Windows Media Format, servicio de administración de licencias
- SDK de Windows Media Format, detección de fraudes
- Administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- Administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), característica de restauración de copia de seguridad
- DRM (administración de derechos digitales), característica de restauración de copia de seguridad
- Administración de derechos digitales (DRM), servicio de administración de licencias
- DRM (administración de derechos digitales), servicio de administración de licencias
- Administración de derechos digitales (DRM), detección de fraudes
- DRM (administración de derechos digitales), detección de fraudes
- copia de seguridad de licencias de DRM
- restauración de licencias de DRM
- licencias, DRM
- licencias, copia de seguridad de DRM
- licencias, restaurar DRM
- Característica de restauración de copia de seguridad
- Servicio de administración de licencias
- detección de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104359479"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Copia de seguridad y restauración de licencias de DRM

Con la característica de restauración de copia de seguridad, los usuarios pueden realizar copias de seguridad y restaurar [*licencias*](wmformat-glossary.md) en el mismo equipo o en otros equipos. Esta característica permite a los usuarios transferir licencias a un nuevo equipo o al mismo equipo (por ejemplo, después de volver a formatear el disco duro). Además, los usuarios pueden reproducir archivos ASF protegidos en más de un equipo.

Para fomentar el uso legítimo de una licencia, una directiva de detección de fraudes restringe el número de veces que se puede restaurar una licencia. Microsoft proporciona un servicio que realiza un seguimiento del número de equipos en los que se ha restaurado una licencia; Si se alcanza un límite, el usuario no podrá restaurar la licencia.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Permitir o denegar el derecho a realizar copias de seguridad y restauraciones

La característica de restauración de copia de seguridad solo funciona con licencias para las que se proporciona la opción de copia de seguridad y restauración. Si los propietarios de contenido o los emisores de licencias no desean esta característica, o si emiten licencias que contienen un estado seguro (como operaciones contables o tiempo limitado), pueden no permitir este derecho.

Cuando no se puede restaurar una licencia porque un usuario no tiene el derecho, se pasa un [*identificador de clave*](wmformat-glossary.md) a la aplicación. Como mínimo, se debe notificar al usuario que no se pudo realizar una copia de seguridad de algunas licencias, aunque el usuario no sabe a qué licencias hace referencia este mensaje. Si conoce el identificador de clave para los archivos protegidos disponibles, puede desarrollar una solución más sólida para informar al usuario.

Por ejemplo, un reproductor podría desarrollarse para una etiqueta de registro que proporcione canciones protegidas en Internet. Se puede realizar un seguimiento de estas canciones y de sus identificadores de clave en una base de datos. Si no se pudo realizar una copia de seguridad de algunas licencias, la aplicación del reproductor podría usar el identificador de clave para consultar el nombre de las canciones en la base de datos y, a continuación, informar al usuario sobre las canciones de las que no se pueden realizar copias de seguridad. O bien, se podría crear una biblioteca de música para cada usuario localmente, y el identificador de clave podría usarse para recuperar más información acerca de las licencias de las que no se pudo realizar una copia de seguridad.

## <a name="the-license-management-service"></a>El servicio de administración de licencias

Cuando se implementa la característica de restauración de copia de seguridad, un servicio de administración de licencias hospedado por Microsoft administra la restauración de licencias.

En primer lugar, los usuarios copian las licencias en la aplicación, por ejemplo, eligiendo una opción de menú. Se realiza una copia de seguridad de todas las licencias del equipo en una ubicación especificada, como un disquete. Después, los usuarios restauran las licencias mediante la aplicación, por ejemplo, eligiendo una opción de menú y especificando su ubicación de copia de seguridad.

En este momento, el usuario debe estar conectado a Internet. una solicitud de la aplicación se envía al servicio de administración de licencias. Si el equipo desde el que se realizó la copia de seguridad de la licencia es diferente del equipo original (o se ha cambiado el formato del equipo original), el servicio de administración de licencias emite una nueva licencia al nuevo equipo. De lo contrario, se reenvía la licencia que se emitió previamente a ese equipo.

Dado que el servicio de administración de licencias recupera información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el [sitio web de Microsoft](https://www.microsoft.com/licensing/default).

> [!Note]  
> Cuando un usuario final restaura una licencia en otro equipo y la licencia requiere la individualización, el usuario final debe autorizar la actualización de los componentes de DRM. Debe implementar un proceso en la aplicación de reproducción para admitir esta característica.

 

## <a name="detecting-fraud"></a>Detección de fraudes

El usuario puede restaurar una licencia un número limitado de veces. Cada vez que se restaura una licencia, el servicio de administración de licencias realiza su seguimiento e incrementa el recuento de esa licencia en uno. Al restaurar una licencia a un equipo en el que se ha restaurado anteriormente la licencia (por ejemplo, el equipo desde el que se realizó la copia de seguridad de la licencia), el recuento no se incrementa. Un equipo se considera diferente si tiene un nuevo sistema operativo o si se ha vuelto a instalar el sistema operativo.

De acuerdo con la Directiva de detección de fraudes de Microsoft, cuando una licencia se ha restaurado un número determinado de veces, la aplicación recibe una dirección URL de los componentes de DRM y es responsable de abrir un explorador y mostrar la página web, lo que indica que es posible que se haya infringido el contrato de licencia. El usuario debe ponerse en contacto con el distribuidor de licencias, que debe determinar si la solicitud es válida.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Copia de seguridad y restauración de licencias**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




