---
description: ASOCIACIÓN DE RED \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c383ac251d410e03fc5d26dd969d4161ae555ebf2cdd3802ca7228b1739ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842295"
---
# <a name="wpd_content_type_network_association"></a>ASOCIACIÓN DE RED \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE NETWORK ASSOCIATION representa una asociación \_ entre un host y un \_ \_ \_ dispositivo.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad         | Obligatorio u opcional        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                                       | Obligatorio.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                                        | Obligatorio.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                                                   | Obligatorio si el objeto representa un archivo.                             |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                                               | Obligatorio.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                                                  | Obligatorio.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                                           | Obligatorio si el objeto está oculto.                                     |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                                           | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                                                   | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                                     | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                                              | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                                       | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                                           | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                                            | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                                         | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                                  | Opcional.                                                             |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                                | Se recomienda su uso.                                                          |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                                       | Se recomienda si otro objeto hace referencia al objeto.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)                            | Opcional.                                                             |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md)                        | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                      | Obligatorio si no se puede eliminar el objeto.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | Opcional.                                                             |
| [IDENTIFICADORES DE \_ RED HOST \_ DE \_ ASOCIACIÓN DE RED DE \_ \_ WPD](network-association-properties.md) | Obligatorio.                                                             |
| [ASOCIACIÓN \_ DE \_ RED \_ WPD X509V3SEQUENCE](network-association-properties.md)                       | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



