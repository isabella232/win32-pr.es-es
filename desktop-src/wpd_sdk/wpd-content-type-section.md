---
description: SECCIÓN TIPO DE \_ CONTENIDO \_ DE \_ WPD
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262071"
---
# <a name="wpd_content_type_section"></a>SECCIÓN TIPO DE \_ CONTENIDO \_ DE \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE SECTION representa una sección de datos contenida \_ \_ en otro \_ objeto. Por ejemplo, un archivo de audio grande se puede describir como una colección de varios capítulos y cada capítulo podría ser un objeto \_ CONTENT TYPE SECTION de WPD. \_ \_

La propiedad WPD \_ OBJECT REFERENCES identifica el objeto primario de una sección \_ determinada.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad       | Obligatorio u opcional             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                           | Necesario.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                            | Necesario.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                                       | Obligatorio si el objeto representa un archivo.                             |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                                     | Necesario.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                                   | Necesario.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                                      | Necesario.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                               | Obligatorio si el objeto está oculto.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                               | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                                       | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                                  | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                           | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                               | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                             | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                                      | Opcional.                                                             |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                                    | Se recomienda su uso.                                                          |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                                    | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                | Se recomienda si el objeto tiene referencias a otros objetos.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)                | Opcional.                                                             |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md)            | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                                          | Obligatorio si no se puede eliminar el objeto.                             |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                           | Opcional.                                                             |
| [DESPLAZAMIENTO DE DATOS \_ DE LA SECCIÓN \_ WPD \_](section-attribute-properties.md)                                           | Necesario.                                                             |
| [LONGITUD DE DATOS \_ DE LA \_ SECCIÓN WPD \_](section-attribute-properties.md)                                           | Necesario.                                                             |
| [UNIDADES DE DATOS \_ DE LA SECCIÓN \_ WPD \_](section-attribute-properties.md)                                             | Se recomienda su uso.                                                          |
| [RECURSO DE OBJETO \_ AL QUE SE HACE REFERENCIA A DATOS DE LA SECCIÓN \_ \_ \_ \_ WPD](section-attribute-properties.md) | Se recomienda su uso.                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



