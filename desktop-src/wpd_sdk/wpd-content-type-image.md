---
description: IMAGEN DE TIPO \_ DE \_ CONTENIDO \_ WPD
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846347ac83345ed685a10739126028ca1728bb16a52fe7083fcc7dd823447c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193499"
---
# <a name="wpd_content_type_image"></a>IMAGEN DE TIPO \_ DE \_ CONTENIDO \_ WPD

Un objeto que describe su tipo como WPD \_ CONTENT TYPE IMAGE representa una imagen \_ \_ fija.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                   |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                                        |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                                        |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                   |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                                        |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                                        |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                            |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                        |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                            |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                          |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                        |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                        |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                           |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                                                        |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                                                     |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                                        |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                       |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                        |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                                        |
| [WPD \_ IMAGE \_ BITDEPTH](image-properties.md)                                                       | Se recomienda su uso.                                                                                     |
| [ESTADO \_ RECORTADO DE \_ LA IMAGEN \_ WPD](image-properties.md)                                          | Opcional.                                                                                        |
| [ESTADO CORREGIDO \_ DEL COLOR DE LA IMAGEN \_ \_ \_ WPD](image-properties.md)                         | Opcional.                                                                                        |
| [WPD \_ IMAGE \_ FNUMBER](image-properties.md)                                                                           | Opcional.                                                                                        |
| [TIEMPO DE EXPOSICIÓN \_ DE \_ LA IMAGEN \_ WPD](image-properties.md)                                                                    | Opcional.                                                                                        |
| [ÍNDICE DE EXPOSICIÓN \_ DE \_ IMÁGENES DE \_ WPD](image-properties.md)                                                                   | Opcional.                                                                                        |
| [RESOLUCIÓN HORIZONTAL DE \_ LA IMAGEN \_ \_ WPD](image-properties.md)                                                            | Opcional.                                                                                        |
| [RESOLUCIÓN \_ VERTICAL DE LA IMAGEN \_ \_ WPD](image-properties.md)                                                              | Opcional.                                                                                        |
| [WPD \_ MEDIA \_ COPYRIGHT](media-properties.md)                                                     | Opcional.                                                                                        |
| [ANCHO DE MEDIOS \_ \_ WPD](media-properties.md)                                                             | Obligatorio.                                                                                        |
| [ALTO DE \_ MEDIOS \_ WPD](media-properties.md)                                                           | Obligatorio.                                                                                        |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                                                            | Se recomienda su uso.                                                                                     |
| [WPD \_ MEDIA \_ ALBUM \_ ARTIST](media-properties.md)                                                                     | Se recomienda su uso. Esta propiedad identifica a la persona o personas que crearon originalmente este objeto. |
| [DIRECCIÓN URL DE \_ ORIGEN MULTIMEDIA DE \_ \_ WPD](media-properties.md)                                                                       | Opcional.                                                                                        |
| [DIRECCIÓN URL DE \_ DESTINO DE MEDIOS DE \_ \_ WPD](media-properties.md)                                                                  | Opcional.                                                                                        |
| [DESCRIPCIÓN DE MEDIOS \_ DE \_ WPD](media-properties.md)                                                                       | Opcional.                                                                                        |
| [GÉNERO MULTIMEDIA DE WPD \_ \_](media-properties.md)                                                                             | Opcional.                                                                                        |
| [MARCADOR DE \_ BYTES MULTIMEDIA \_ WPD \_](media-properties.md)                                                                    | Opcional.                                                                                        |
| [GUID DE \_ MEDIOS DE \_ WPD](media-properties.md)                                                                              | Opcional.                                                                                        |
| [WPD \_ MEDIA \_ SUB \_ DESCRIPTION](media-properties.md)                                                                  | Opcional.                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                                 | Obligatorio u opcional | Descripción                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)        | Obligatorio.            | Contiene los datos de la imagen.                                                                 |
| [**MINIATURA DE RECURSOS DE WPD \_ \_**](wpd-resource-thumbnail.md)    | Se recomienda su uso.         | Contiene la miniatura de la imagen.                                                    |
| [**CLIP DE \_ AUDIO DE \_ RECURSOS WPD \_**](wpd-resource-audio-clip.md) | Opcional.            | Si esta imagen tiene una anotación de audio asociada, este recurso contiene los datos de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



