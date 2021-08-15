---
description: OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58121d351219c246117106d578ed3672ebf25eecf9e159f957494b5c5eae9280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193529"
---
# <a name="wpd_content_type_functional_object"></a>OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD

Un objeto que describe su tipo como WPD CONTENT FUNCTIONAL OBJECT representa \_ \_ un objeto \_ funcional, encapsulando la funcionalidad del dispositivo.

Todos los objetos funcionales, independientemente del tipo, admiten las siguientes propiedades. (Si define un objeto funcional personalizado, también debe admitir estas propiedades).



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.        |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                             |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.        |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                     |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                 |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                 |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                                             |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                                          |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                             |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                             |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                             |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                                             |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](miscellaneous-properties.md)                      | Obligatorio. Consulte la tabla siguiente para ver las categorías definidas por Windows dispositivos portátiles. |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="functional-object-categories"></a>Categorías de objetos funcionales

Los objetos funcionales se pueden agrupar en categorías, en función de sus funciones. Una categoría se describe mediante la propiedad \_ WPD FUNCTIONAL \_ OBJECT CATEGORY \_ (un valor GUID). La categoría determina qué propiedades adicionales se admiten.

En la tabla siguiente se describen las categorías definidas por Windows dispositivos portátiles. Consulte la descripción de la categoría para obtener información sobre qué propiedades y recursos adicionales admite el objeto.



| Categoría funcional                                                                                        | Descripción                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CATEGORÍA FUNCIONAL DE WPD \_ \_ \_ ALL**](wpd-functional-category-all.md)                                      | Esta categoría funcional solo es válida como parámetro para determinadas funciones de consulta (para indicar que todos los tipos de objetos funcionales son aceptables) y no es una categoría funcional notificada por el controlador. |
| [**CAPTURA DE AUDIO \_ DE CATEGORÍA FUNCIONAL DE \_ \_ \_ WPD**](wpd-functional-category-audio-capture.md)                 | El objeto encapsula la funcionalidad de captura de audio en el dispositivo, por ejemplo, una grabadora de voz u otro componente de grabación de audio.                                                                      |
| [**DISPOSITIVO DE CATEGORÍA \_ FUNCIONAL \_ \_ WPD**](wpd-functional-category-device.md)                                | El objeto encapsula el dispositivo (es decir, el objeto de nivel superior del dispositivo).                                                                                                                          |
| [**CONFIGURACIÓN DE RED \_ DE \_ CATEGORÍA FUNCIONAL \_ DE \_ WPD**](wpd-functional-category-network-configuration.md) | El objeto encapsula la funcionalidad de configuración de red para el dispositivo, por ejemplo, perfiles de Wi-Fi o asociaciones.                                                                                   |
| [**INFORMACIÓN DE REPRESENTACIÓN \_ DE \_ CATEGORÍAS FUNCIONALES DE \_ \_ WPD**](wpd-functional-category-rendering-information.md) | El objeto describe los tipos de archivos multimedia que el dispositivo puede reproducir.                                                                                                                            |
| [**SMS DE CATEGORÍA \_ FUNCIONAL \_ DE \_ WPD**](wpd-functional-category-sms.md)                                      | El objeto encapsula la funcionalidad del servicio de mensajes cortos (normalmente denominada "mensajería de texto") en el dispositivo.                                                                                             |
| [**CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA FUNCIONAL \_ \_ DE \_ \_ WPD**](wpd-functional-category-still-image-capture.md)    | El objeto encapsula la funcionalidad de captura de imágenes fijas en un dispositivo, como una cámara o los datos adjuntos de la cámara.                                                                                              |
| [**ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE \_ WPD**](wpd-functional-category-storage.md)                              | El objeto encapsula el almacenamiento físico de archivos en el dispositivo.                                                                                                                                              |
| [**CAPTURA DE VÍDEO \_ DE CATEGORÍA FUNCIONAL DE \_ \_ \_ WPD**](wpd-functional-category-video-capture.md)                 | El objeto encapsula la funcionalidad de captura de vídeo en el dispositivo, por ejemplo, un componente de grabadora de vídeo. Una aplicación usa este objeto para obtener control mediante programación.                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



