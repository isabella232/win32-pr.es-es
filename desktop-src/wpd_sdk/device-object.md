---
description: Objeto de dispositivo
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Objeto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef76dbe26b1fd2c8d2bfd6da708728c9eb2177b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541238"
---
# <a name="device-object"></a>Objeto de dispositivo

El objeto de dispositivo admite las siguientes propiedades. Una aplicación puede solicitar estas propiedades consultando el objeto raíz (especificando el identificador de objeto constante de **\_ identificador de \_ objeto \_ de dispositivo WPD** ). Todos los valores del objeto de dispositivo son de solo lectura.

Si un dispositivo determinado implementa la categoría [de \_ \_ \_ dispositivo de categoría funcional de WPD](wpd-functional-category-device.md) , también debe admitir las propiedades asociadas a esa categoría.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Obligatorio. El valor es **el \_ \_ \_ identificador de objeto de dispositivo WPD**.                                                         |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio. El valor es una cadena vacía.                                                                     |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                                                   |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Obligatorio.                                                                                                   |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Obligatorio si el objeto de dispositivo no se debe mostrar al usuario.                                              |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto de dispositivo tiene referencias a otros objetos.                                              |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                                   |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                   |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                                   |
| [\_asociado de \_ sincronización de dispositivos de WPD \_](device-properties.md)                                           | Opcional.                                                                                                   |
| [\_versión de \_ firmware del dispositivo WPD \_](device-properties.md)                                   | Obligatorio.                                                                                                   |
| [\_nivel de \_ energía del dispositivo WPD \_](device-properties.md)                                             | Se recomienda si el dispositivo tiene una batería.                                                                    |
| [\_fuente de \_ alimentación del dispositivo de WPD \_](device-properties.md)                                           | Se recomienda su uso.                                                                                                |
| [\_Protocolo de dispositivo WPD \_](device-properties.md)                                                    | Se recomienda su uso.                                                                                                |
| [\_ \_ fabricante del dispositivo WPD](device-properties.md)                                            | Obligatorio.                                                                                                   |
| [\_modelo de dispositivo de WPD \_](device-properties.md)                                                          | Obligatorio.                                                                                                   |
| [\_número de \_ serie del dispositivo WPD \_](device-properties.md)                                         | Obligatorio.                                                                                                   |
| [el \_ dispositivo WPD \_ admite valores \_ no \_ consumibles](device-properties.md)                    | Requerido si el dispositivo admite objetos no consumibles; es decir, si se puede usar para el almacenamiento de datos simple. |
| [\_ \_ fecha y hora del dispositivo WPD](device-properties.md)                                                    | Opcional.                                                                                                   |
| [\_ \_ nombre descriptivo del dispositivo WPD \_](device-properties.md)                                         | Se recomienda su uso.                                                                                                |
| [\_ \_ esquema DRM compatible con dispositivos \_ WPD \_](device-properties.md)                          | Se recomienda si el dispositivo admite Rights Management digitales (DRM).                                         |
| [los \_ \_ formatos admitidos del dispositivo WPD \_ \_ están \_ ordenados](device-properties.md)       | Se recomienda si el dispositivo admite el orden de formato preferido.                                               |
| [\_tipo de dispositivo WPD \_](device-properties.md)                                                            | Se recomienda su uso.                                                                                                |
| [\_ \_ \_ identificador único funcional del dispositivo WPD \_](device-properties.md)                          | Opcional.                                                                                                   |
| [\_ \_ identificador único del modelo de dispositivo de \_ WPD \_](device-properties.md)                                    | Opcional.                                                                                                   |
| [\_transporte de dispositivo WPD \_](device-properties.md)                                                  | Se recomienda su uso.                                                                                                |
| [dispositivo de uso de la \_ \_ \_ fase de dispositivo \_ WPD](device-properties.md)                                  | Opcional.                                                                                                   |
| [\_categoría de \_ objeto \_ funcional de WPD](device-properties.md)                             | Obligatorio.                                                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="commands"></a>Comandos:

Además de las propiedades, los dispositivos deben admitir un conjunto específico de comandos definidos por dispositivos portátiles de Windows. Los comandos que admite un objeto o un dispositivo dependen del tipo, la funcionalidad y las capacidades.

En la tabla siguiente se describen las clases de comandos que se aplican a los dispositivos, por funcionalidad. Normalmente, un dispositivo se encuentra en varias categorías y debe admitir los comandos para todas las categorías aplicables. Por ejemplo, un teléfono móvil con una cámara estaría en tres categorías: todos los dispositivos, los dispositivos SMS y los dispositivos de captura de imagen. Un controlador personalizado y una aplicación cliente pueden admitir comandos o propiedades adicionales que se definen, pero deben admitir los siguientes comandos. Para obtener una descripción de los comandos específicos que se encuentran bajo cada categoría de comandos, vea [comandos](commands.md).



| Descripción                                                                                                                                                                                                                      | Categorías de comandos                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Todos los dispositivos.                                                                                                                                                                                                                     | **Categoría común de la categoría \_ \_ CAPABILITIESWPD de \_ WPD \_**<br/> **\_ \_ enumeración de objetos de categoría de WPD \_**<br/> **\_Administración de \_ objetos de categoría de WPD \_**<br/> **\_propiedades del \_ objeto de categoría de WPD \_**<br/> **propiedades de objeto de categoría de WPD \_ \_ \_ \_ bulk**<br/> **\_recursos de \_ objeto de categoría de WPD \_**<br/> |
| Dispositivos que pueden capturar imágenes fijas, como cámaras digitales.                                                                                                                                                                  | **\_captura de \_ \_ imagen \_ de la categoría de WPD**                                                                                                                                                                                                                                                                                   |
| Dispositivos que pueden enviar mensajes de servicio de mensajes cortos (SMS), como teléfonos móviles. El envío de mensajes SMS se denomina a menudo "mensajería de texto".                                                                                      | **\_SMS categoría de WPD \_**                                                                                                                                                                                                                                                                                                     |
| Dispositivos que funcionan como dispositivos de almacenamiento. Entre ellas se incluyen las unidades externas. Si un dispositivo admite la capacidad de formatear un almacén o de trasladar objetos de una ubicación a otra, el controlador debe admitir esta categoría.<br/> | **\_almacenamiento de categorías de WPD \_**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




