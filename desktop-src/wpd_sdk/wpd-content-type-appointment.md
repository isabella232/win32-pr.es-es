---
description: CITA DE \_ TIPO DE \_ CONTENIDO WPD \_
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159f80246b14c121e386f1122a70dce27e717481ec02897c06b9061821a8c0fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193549"
---
# <a name="wpd_content_type_appointment"></a>CITA DE \_ TIPO DE \_ CONTENIDO WPD \_

Un objeto que describe su tipo como WPD \_ CONTENT TYPE APPOINTMENT representa una cita en un \_ \_ calendario.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                      |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                      |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                      |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                              |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
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
| [UBICACIÓN DE CITA \_ DE \_ WPD](appointment-properties.md)                                     | Obligatorio.                                                                      |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si el objeto se puede eliminar.                                         |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                      |
| [ASUNTO DE \_ INFORMACIÓN COMÚN \_ DE \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                      |
| [TEXTO DEL CUERPO \_ DE INFORMACIÓN COMÚN DE \_ \_ \_ WPD](object-properties.md)                                                         | Se recomienda su uso.                                                                   |
| [PRIORIDAD DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD](object-properties.md)                                                           | Se recomienda su uso.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME](object-properties.md)                                                    | Se recomienda su uso.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME](object-properties.md)                                                      | Se recomienda su uso.                                                                   |
| [NOTAS DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [UBICACIÓN DE CITA \_ DE \_ WPD](object-properties.md)                                                                   | Obligatorio.                                                                      |
| [TIPO DE \_ CITA \_ WPD](appointment-properties.md)                                             | Opcional.                                                                      |
| [ASISTENTES NECESARIOS \_ PARA \_ LA CITA DE WPD \_](appointment-properties.md)                | Opcional.                                                                      |
| [ASISTENTES \_ \_ OPCIONALES A LA CITA \_ DE WPD](appointment-properties.md)                | Opcional.                                                                      |
| [ASISTENTES \_ \_ ACEPTADOS EN LA CITA \_ DE WPD](appointment-properties.md)                | Opcional.                                                                      |
| [RECURSOS DE CITAS DE WPD \_ \_](appointment-properties.md)                                   | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



