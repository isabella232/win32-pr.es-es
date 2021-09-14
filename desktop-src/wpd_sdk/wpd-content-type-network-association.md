---
description: ASOCIACIÓN DE \_ RED DE TIPO DE CONTENIDO \_ \_ \_ WPD
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c92f76080db4167a12578c58e9d85c9506c28b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266804"
---
# <a name="wpd_content_type_network_association"></a>ASOCIACIÓN DE \_ RED DE TIPO DE CONTENIDO \_ \_ \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE NETWORK ASSOCIATION representa una asociación \_ entre un host y un \_ \_ \_ dispositivo.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad         | Obligatorio u opcional        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                                       | Necesario.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                                        | Necesario.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                                                   | Obligatorio si el objeto representa un archivo.                             |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                                                 | Necesario.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                                               | Necesario.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                                                  | Necesario.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                                           | Obligatorio si el objeto está oculto.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                                           | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                                                   | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                                     | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                                              | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                                       | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                                           | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                                            | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                                         | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                                                  | Opcional.                                                             |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                                                | Se recomienda su uso.                                                          |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                                       | Se recomienda si otro objeto hace referencia al objeto.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)                            | Opcional.                                                             |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md)                        | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                                                      | Obligatorio si no se puede eliminar el objeto.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | Opcional.                                                             |
| [IDENTIFICADORES DE \_ RED DE HOST DE \_ \_ \_ ASOCIACIÓN DE REDES \_ WPD](network-association-properties.md) | Necesario.                                                             |
| [WPD \_ NETWORK \_ ASSOCIATION \_ X509V3SEQUENCE](network-association-properties.md)                       | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



