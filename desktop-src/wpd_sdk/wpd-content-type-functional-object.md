---
description: '\_ \_ objeto funcional de tipo de contenido de \_ WPD \_'
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8516d29bf08b4873dc80c72b9a23de19dc50d0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678275"
---
# <a name="wpd_content_type_functional_object"></a>\_ \_ objeto funcional de tipo de contenido de \_ WPD \_

Objeto que describe su tipo como \_ objeto funcional de contenido de WPD \_ \_ representa un objeto funcional, encapsulando la funcionalidad del dispositivo.

Todos los objetos funcionales, independientemente del tipo, admiten las siguientes propiedades. (Si define un objeto funcional personalizado, también debe admitir estas propiedades).



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.        |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                             |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Obligatorio.                                                                             |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.        |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                             |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                             |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                     |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                 |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                     |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                             |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                 |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                               |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                             |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                             |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                             |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                          |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                             |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                            |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                             |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                             |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                             |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                             |
| [\_categoría de \_ objeto \_ funcional de WPD](miscellaneous-properties.md)                      | Obligatorio. Vea la tabla siguiente para ver las categorías definidas por dispositivos portátiles de Windows. |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="functional-object-categories"></a>Categorías de objetos funcionales

Los objetos funcionales se pueden agrupar en categorías, en función de sus funciones. Una categoría se describe mediante la \_ \_ propiedad categoría de objeto funcional WPD \_ (un valor GUID). La categoría determina qué propiedades adicionales se admiten.

En la tabla siguiente se describen las categorías definidas por dispositivos portátiles de Windows. Vea la descripción de la categoría para obtener información sobre qué propiedades y recursos adicionales admite el objeto.



| Categoría funcional                                                                                        | Descripción                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_categoría funcional \_ \_ todo en WPD**](wpd-functional-category-all.md)                                      | Esta categoría funcional solo es válida como parámetro para ciertas funciones de consulta (para indicar que todos los tipos de objeto funcionales son aceptables) y no es una categoría funcional notificada por el controlador. |
| [**\_captura de \_ audio de categoría funcional \_ de WPD \_**](wpd-functional-category-audio-capture.md)                 | El objeto encapsula la funcionalidad de captura de audio en el dispositivo, por ejemplo, una grabadora de voz u otro componente de grabación de audio.                                                                      |
| [**\_dispositivo de \_ categoría \_ funcional de WPD**](wpd-functional-category-device.md)                                | El objeto encapsula el dispositivo (es decir, el objeto de nivel superior del dispositivo).                                                                                                                          |
| [**\_configuración de \_ red de categoría funcional \_ de WPD \_**](wpd-functional-category-network-configuration.md) | El objeto encapsula la funcionalidad de configuración de red para el dispositivo, por ejemplo, perfiles de Wi-Fi o asociaciones.                                                                                   |
| [**\_información de \_ representación de categoría funcional \_ de WPD \_**](wpd-functional-category-rendering-information.md) | El objeto describe los tipos de archivos multimedia que el dispositivo puede reproducir.                                                                                                                            |
| [**\_SMS de \_ categoría \_ funcional de WPD**](wpd-functional-category-sms.md)                                      | El objeto encapsula la funcionalidad de servicio de mensajes cortos (denominada comúnmente "mensajería de texto") en el dispositivo.                                                                                             |
| [**\_captura de \_ imagen de categoría funcional de \_ WPD \_ \_**](wpd-functional-category-still-image-capture.md)    | El objeto encapsula la funcionalidad de captura de imagen en un dispositivo, como un archivo adjunto de cámara o cámara.                                                                                              |
| [**\_almacenamiento de \_ categoría \_ funcional de WPD**](wpd-functional-category-storage.md)                              | El objeto encapsula el almacenamiento de archivos físico en el dispositivo.                                                                                                                                              |
| [**\_captura de \_ vídeo de categoría funcional \_ de WPD \_**](wpd-functional-category-video-capture.md)                 | El objeto encapsula la funcionalidad de captura de vídeo en el dispositivo, por ejemplo, un componente de grabadora de vídeo. Una aplicación usa este objeto para obtener el control mediante programación.                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



