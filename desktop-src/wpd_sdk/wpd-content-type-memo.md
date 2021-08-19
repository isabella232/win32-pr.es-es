---
description: WPD \_ CONTENT \_ TYPE \_ MEMO
ms.assetid: 6d89681c-1183-44d3-a39e-5fb343f1abbe
title: WPD_CONTENT_TYPE_MEMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563148d28a03558843060bedfb76a6f91ca6805c0498e8a8d66e3dd53a68ed82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006045"
---
# <a name="wpd_content_type_memo"></a>WPD \_ CONTENT \_ TYPE \_ MEMO

Un objeto que describe su tipo como WPD \_ CONTENT TYPE MEMO representa una nota de \_ \_ texto.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad      |   Obligatorio u opcional      |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación. |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                      |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                      |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad ni siquiera en el momento de la creación.  |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                      |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                      |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                              |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).          |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                              |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                      |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.          |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                        |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                      |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                      |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                         |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                                      |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                                   |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                      |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                     |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                      |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                      |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                      |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                                      |
| [ASUNTO DE INFORMACIÓN \_ COMÚN \_ DE \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                      |
| [TEXTO DEL CUERPO \_ DE INFORMACIÓN COMÚN DE \_ \_ \_ WPD](object-properties.md)                                                         | Se recomienda su uso.                                                                   |
| [PRIORIDAD DE INFORMACIÓN \_ \_ COMÚN DE \_ WPD](object-properties.md)                                                           | Se recomienda su uso.                                                                   |
| [FECHA Y HORA DE INICIO DE INFORMACIÓN COMÚN \_ \_ \_ \_ DE WPD](object-properties.md)                                                    | Se recomienda su uso.                                                                   |
| [FECHA Y HORA DE FINALIZACIÓN DE INFORMACIÓN COMÚN \_ \_ \_ \_ DE WPD](object-properties.md)                                                      | Se recomienda su uso.                                                                   |
| [NOTAS DE INFORMACIÓN \_ \_ COMUNES DE \_ WPD](object-properties.md)                                                              | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



