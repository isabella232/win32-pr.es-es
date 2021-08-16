---
description: DISPOSITIVO DE CATEGORÍA \_ FUNCIONAL \_ WPD \_
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842221"
---
# <a name="wpd_functional_category_device"></a>DISPOSITIVO DE CATEGORÍA \_ FUNCIONAL \_ WPD \_

Un objeto funcional WPD FUNCTIONAL CATEGORY DEVICE encapsula el dispositivo (es decir, el objeto de nivel \_ \_ superior del \_ dispositivo). Si un dispositivo implementa esta categoría funcional, debe admitir estas propiedades además de las propiedades enumeradas para el objeto [de dispositivo](device-object.md).



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                      |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                                                           |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                                                           |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                      |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                                                           |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                                                           |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                                   |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                               |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                   |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                                           |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                               |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                             |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                           |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                           |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                              |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                                                                           |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                                                                        |
| [FECHA DE \_ CREACIÓN DEL \_ OBJETO \_ WPD](object-properties.md)                                         | Opcional.                                                                                                           |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                          |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                           |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                                                                           |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](miscellaneous-properties.md)                      | Obligatorio.                                                                                                           |
| [WPD \_ DEVICE \_ SYNC \_ PARTNER](device-properties.md)                                           | Opcional.                                                                                                           |
| [VERSIÓN DEL \_ \_ FIRMWARE DEL DISPOSITIVO \_ WPD](device-properties.md)                                   | Obligatorio.                                                                                                           |
| [NIVEL DE \_ ENERGÍA DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                             | Se recomienda si el dispositivo tiene una batería.                                                                                |
| [FUENTE DE \_ ALIMENTACIÓN DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                           | Se recomienda su uso.                                                                                                        |
| [PROTOCOLO DE DISPOSITIVO \_ \_ WPD](device-properties.md)                                                    | Se recomienda su uso.                                                                                                        |
| [FABRICANTE DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                            | Obligatorio.                                                                                                           |
| [MODELO DE \_ DISPOSITIVO \_ WPD](device-properties.md)                                                          | Obligatorio.                                                                                                           |
| [NÚMERO DE SERIE \_ DEL DISPOSITIVO \_ \_ WPD](device-properties.md)                                         | Obligatorio.                                                                                                           |
| [EL DISPOSITIVO WPD \_ \_ ADMITE \_ DISPOSITIVOS NO \_ CONSUMIBLES](device-properties.md)                    | Obligatorio si el dispositivo admite objetos no consumibles; es decir, si el dispositivo se puede usar para el almacenamiento de datos simple. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Opcional.                                                                                                           |
| [NOMBRE DESCRIPTIVO \_ DEL DISPOSITIVO \_ \_ WPD](device-properties.md)                                         | Se recomienda su uso.                                                                                                        |
| [ESQUEMAS DRM \_ COMPATIBLES \_ CON \_ DISPOSITIVOS WPD \_](device-properties.md)                        | Se recomienda si el dispositivo admite tecnología DRM.                                                                  |
| [SE \_ ORDENAN LOS \_ \_ FORMATOS COMPATIBLES \_ CON DISPOSITIVOS \_ WPD](device-properties.md)       | Se recomienda si el dispositivo admite el orden de formato preferido.                                                       |
| [TIPO DE \_ DISPOSITIVO \_ WPD](device-properties.md)                                                            | Se recomienda su uso.                                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



