---
description: SECCIÓN TIPO \_ DE CONTENIDO \_ DE \_ WPD
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be521313b2401166e4af1be06bf0e5bbe611de3a247a202177d7564f0c759bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927705"
---
# <a name="wpd_content_type_section"></a>SECCIÓN TIPO \_ DE CONTENIDO \_ DE \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE SECTION representa una sección de datos que \_ se encuentra en otro \_ \_ objeto. Por ejemplo, un archivo de audio grande se puede describir como una colección de varios capítulos y cada capítulo podría ser un objeto \_ CONTENT TYPE SECTION de \_ \_ WPD.

La propiedad WPD \_ OBJECT REFERENCES identifica el objeto primario de una sección \_ determinada.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad       | Obligatorio u opcional             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                           | Obligatorio.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                                       | Obligatorio si el objeto representa un archivo.                             |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                     | Obligatorio.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                                   | Obligatorio.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                                      | Obligatorio.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                               | Obligatorio si el objeto está oculto.                                     |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                               | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                                       | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                                  | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                           | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                               | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                             | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                      | Opcional.                                                             |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                    | Se recomienda su uso.                                                          |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                    | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                | Se recomienda si el objeto tiene referencias a otros objetos.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)                | Opcional.                                                             |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md)            | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                          | Obligatorio si no se puede eliminar el objeto.                             |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                           | Opcional.                                                             |
| [DESPLAZAMIENTO DE DATOS \_ DE LA SECCIÓN \_ \_ WPD](section-attribute-properties.md)                                           | Obligatorio.                                                             |
| [LONGITUD DE DATOS \_ DE LA SECCIÓN \_ \_ WPD](section-attribute-properties.md)                                           | Obligatorio.                                                             |
| [UNIDADES DE \_ DATOS DE LA SECCIÓN \_ WPD \_](section-attribute-properties.md)                                             | Se recomienda su uso.                                                          |
| [RECURSO DE OBJETO \_ AL QUE SE HACE REFERENCIA EN DATOS DE LA SECCIÓN \_ \_ \_ \_ WPD](section-attribute-properties.md) | Se recomienda su uso.                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



