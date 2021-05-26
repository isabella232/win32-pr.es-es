---
description: TAREA TIPO \_ DE \_ CONTENIDO \_ WPD
ms.assetid: 503d0b11-2113-4df4-8b6b-250f24d09b1f
title: WPD_CONTENT_TYPE_TASK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6823a6707cac184ca5e04eda90a036f39f7b89a8
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424325"
---
# <a name="wpd_content_type_task"></a>TAREA TIPO \_ DE \_ CONTENIDO \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE TASK representa una tarea, como un \_ elemento de una lista de \_ \_ tareas.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad       | Obligatorio u opcional         |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                      |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                                      |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                                      |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                              |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                              |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                      |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.          |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                        |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                      |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                      |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                         |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                                      |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                                   |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                      |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                     |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                      |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                                      |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                      |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                                      |
| [ASUNTO DE INFORMACIÓN \_ COMÚN \_ DE \_ WPD](object-properties.md)                                                            | Necesario.                                                                      |
| [TEXTO DEL CUERPO \_ DE INFORMACIÓN COMÚN DE \_ \_ \_ WPD](object-properties.md)                                                         | Se recomienda su uso.                                                                   |
| [PRIORIDAD DE INFORMACIÓN \_ \_ COMÚN DE \_ WPD](object-properties.md)                                                           | Se recomienda su uso.                                                                   |
| [FECHA Y HORA DE INICIO DE INFORMACIÓN COMÚN \_ \_ \_ \_ DE WPD](object-properties.md)                                                    | Se recomienda su uso.                                                                   |
| [FECHA Y HORA DE FINALIZACIÓN DE INFORMACIÓN COMÚN \_ \_ \_ \_ DE WPD](object-properties.md)                                                      | Se recomienda su uso.                                                                   |
| [NOTAS DE INFORMACIÓN \_ \_ COMUNES DE \_ WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [ESTADO DE LA \_ TAREA WPD \_](task-properties.md)                                                              | Opcional.                                                                      |
| [PORCENTAJE DE TAREAS DE WPD \_ \_ \_ COMPLETADAS](task-properties.md)                                         | Opcional.                                                                      |
| [FECHA DEL RECORDATORIO \_ DE \_ LA TAREA \_ WPD](task-properties.md)                                               | Opcional.                                                                      |
| [PROPIETARIO DE LA \_ TAREA \_ WPD](task-properties.md)                                                                | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



