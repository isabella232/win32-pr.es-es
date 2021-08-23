---
description: CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA FUNCIONAL \_ \_ DE \_ \_ WPD
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fb0f6f19930780784083eaeddc1156bf55c99943aae8ad5850374c04211dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444815"
---
# <a name="wpd_functional_category_still_image_capture"></a>CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA FUNCIONAL \_ \_ DE \_ \_ WPD

Un objeto funcional WPD FUNCTIONAL CATEGORY STILL IMAGE CAPTURE encapsula la funcionalidad de captura de imágenes fijas en un dispositivo, como una cámara o un archivo \_ \_ adjunto de la \_ \_ \_ cámara.



| Nombre de la propiedad                                                                                                            | Obligatorio u opcional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                   | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                    | Obligatorio.                                                                                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                               | Obligatorio.                                                                                                                                              |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                             | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                           | Obligatorio.                                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                              | Obligatorio.                                                                                                                                              |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                       | Obligatorio si el objeto está oculto.                                                                                                                      |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                       | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                               | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                                 | Obligatorio si el objeto representa un archivo.                                                                                                              |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                          | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                                                                  |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                   | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                       | Opcional.                                                                                                                                              |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                        | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                     | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                              | Opcional.                                                                                                                                              |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                            | Se recomienda su uso.                                                                                                                                           |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                            | Opcional.                                                                                                                                              |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                   | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)        | Opcional.                                                                                                                                              |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md)    | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                        | Obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                   | Opcional.                                                                                                                                              |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](miscellaneous-properties.md)                         | Obligatorio. Vea WPD CONTENT TYPE FUNCTIONAL OBJECT (OBJETO FUNCIONAL DE TIPO DE [**\_ CONTENIDO DE \_ \_ \_ WPD)**](wpd-content-type-functional-object.md) para ver las categorías definidas Windows dispositivos portátiles. |
| [RESOLUCIÓN DE CAPTURA \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                  | Obligatorio.                                                                                                                                              |
| [FORMATO DE CAPTURA \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                          | Obligatorio.                                                                                                                                              |
| [CONFIGURACIÓN DE COMPRESIÓN \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                | Opcional.                                                                                                                                              |
| [BALANCE DE BLANCO DE LA IMAGEN DE WPD \_ \_ STILL \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [GANANCIA RGB \_ DE LA IMAGEN DE \_ \_ WPD \_ STILL](still-image-properties.md)                                      | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FNUMBER](still-image-properties.md)                                         | Opcional.                                                                                                                                              |
| [LONGITUD FOCAL DE \_ LA IMAGEN DE \_ \_ WPD STILL \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [DISTANCIA DE \_ FOCO DE LA IMAGEN DE WPD \_ \_ \_ STILL](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [MODO DE \_ ENFOQUE DE IMAGEN DE \_ \_ \_ WPD STILL](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [MODO DE \_ MEDICIÓN DE \_ EXPOSICIÓN DE \_ IMÁGENES \_ \_ DE WPD STILL](still-image-properties.md)         | Opcional.                                                                                                                                              |
| [MODO FLASH \_ DE IMAGEN DE WPD STILL \_ \_ \_](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [TIEMPO DE EXPOSICIÓN \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [MODO DEL PROGRAMA \_ DE EXPOSICIÓN DE IMÁGENES \_ \_ DE \_ \_ WPD STILL](still-image-properties.md)           | Opcional.                                                                                                                                              |
| [ÍNDICE DE EXPOSICIÓN \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [COMPENSACIÓN DE \_ \_ SESGO \_ DE EXPOSICIÓN DE \_ IMÁGENES \_ DE WPD STILL](still-image-properties.md) | Opcional.                                                                                                                                              |
| [RETRASO DE CAPTURA \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [MODO DE CAPTURA \_ DE IMÁGENES DE WPD STILL \_ \_ \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [CONTRASTE DE LA \_ IMAGEN DE WPD \_ STILL \_](still-image-properties.md)                                       | Opcional.                                                                                                                                              |
| [NICIDAD DE \_ LA \_ IMAGEN DE \_ WPD STILL](still-image-properties.md)                                     | Opcional.                                                                                                                                              |
| [ZOOM DIGITAL \_ DE LA IMAGEN DE WPD STILL \_ \_ \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [MODO DE EFECTO \_ DE IMAGEN \_ DE \_ \_ WPD STILL](still-image-properties.md)                                | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ BURST \_ NUMBER](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [INTERVALO DE RÁFAGA DE IMAGEN DE WPD \_ STILL \_ \_ \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ NUMBER](still-image-properties.md)                      | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ INTERVAL](still-image-properties.md)                  | Opcional.                                                                                                                                              |
| [MODO DE \_ MEDICIÓN DE \_ FOCO DE IMÁGENES \_ DE \_ \_ WPD STILL](still-image-properties.md)               | Opcional.                                                                                                                                              |
| [DIRECCIÓN URL DE \_ CARGA DE LA IMAGEN DE \_ \_ \_ WPD STILL](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ ARTIST](still-image-properties.md)                                           | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

Muchas de estas propiedades tienen efectos interconectados. Por ejemplo, si **WPD \_ STILL IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE** está establecido en automático, se vincularán el valor f-stop, el tiempo de exposición y el medidor de exposición; si varía uno, los demás variarán.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



