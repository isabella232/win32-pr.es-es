---
description: SMS DE CATEGORÍA FUNCIONAL DE WPD \_ \_ \_
ms.assetid: dbb536a6-9c12-459d-8098-ebe4fc4c8f2f
title: WPD_FUNCTIONAL_CATEGORY_SMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273807900639f7c220bbb1828233bd717a8b814160167df3be87bda904d5a3e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838935"
---
# <a name="wpd_functional_category_sms"></a>SMS DE CATEGORÍA FUNCIONAL DE WPD \_ \_ \_

Un objeto funcional SMS DE CATEGORÍA FUNCIONAL DE WPD encapsula la funcionalidad del servicio de mensajes corta (normalmente denominada "mensajería de \_ \_ \_ texto") en el dispositivo.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                                                                                              |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                                                                                              |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                                                                      |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                                                                              |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                                                                  |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                                                                                                           |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                                              |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](miscellaneous-properties.md)                      | Obligatorio. Vea [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OBJETO FUNCIONAL DE**](wpd-content-type-functional-object.md) TIPO DE CONTENIDO DE WPD) para ver las categorías definidas Windows dispositivos portátiles. |
| [PROVEEDOR DE \_ SMS \_ WPD](sms-properties.md)                                                             | Obligatorio.                                                                                                                                              |
| [TIEMPO DE ESPERA DE SMS DE WPD \_ \_](sms-properties.md)                                                               | Obligatorio.                                                                                                                                              |
| [CARGA MÁXIMA DE \_ SMS \_ WPD \_](sms-properties.md)                                                      | Obligatorio.                                                                                                                                              |
| [CODIFICACIÓN \_ DE SMS \_ WPD](sms-properties.md)                                                             | Obligatorio.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



