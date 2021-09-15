---
description: CERTIFICADO DE TIPO \_ DE \_ CONTENIDO \_ WPD
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466194"
---
# <a name="wpd_content_type_certificate"></a>CERTIFICADO DE TIPO \_ DE \_ CONTENIDO \_ WPD

Un objeto que describe su tipo como WPD \_ CONTENT TYPE CERTIFICATE representa un certificado usado para la \_ \_ autenticación.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Necesario.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                             |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Necesario.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                     |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                             |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                          |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                     | Se recomienda si otro objeto hace referencia al objeto.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                             |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                               | Obligatorio si se puede eliminar el objeto.                                |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional | Descripción        |
|--------------------------------------------------------|----------------------|--------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md) | Necesario.            | Contiene los datos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



