---
description: Objeto Device
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Objeto Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5279f63c7dabd8bd5b523d9234e33a60d9cf05608ac7b3f1b7601fd8c25024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083619"
---
# <a name="device-object"></a>Objeto Device

El objeto de dispositivo admite las siguientes propiedades. Una aplicación puede solicitar estas propiedades consultando el objeto raíz (especificando el identificador de objeto constante de ID DE OBJETO DE DISPOSITIVO DE **WPD \_ \_ \_** definido). Todos los valores del objeto de dispositivo son de solo lectura.

Si un dispositivo determinado implementa la categoría [ \_ WPD FUNCTIONAL \_ CATEGORY \_ DEVICE,](wpd-functional-category-device.md) también debe admitir las propiedades asociadas a esa categoría.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio. El valor es **WPD \_ DEVICE OBJECT \_ \_ ID**.                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio. El valor es una cadena vacía.                                                                     |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                                                                   |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio.                                                                                                   |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto de dispositivo no se debe mostrar al usuario.                                              |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto de dispositivo tiene referencias a otros objetos.                                              |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                   |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                   |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                                                   |
| [ASOCIADO DE \_ SINCRONIZACIÓN \_ DE DISPOSITIVOS \_ WPD](device-properties.md)                                           | Opcional.                                                                                                   |
| [VERSIÓN DE \_ \_ FIRMWARE DEL DISPOSITIVO \_ WPD](device-properties.md)                                   | Obligatorio.                                                                                                   |
| [NIVEL DE \_ ENERGÍA DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                             | Se recomienda si el dispositivo tiene una batería.                                                                    |
| [FUENTE DE \_ ALIMENTACIÓN DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                           | Se recomienda su uso.                                                                                                |
| [PROTOCOLO DE \_ DISPOSITIVO \_ WPD](device-properties.md)                                                    | Se recomienda su uso.                                                                                                |
| [FABRICANTE DEL \_ DISPOSITIVO \_ WPD](device-properties.md)                                            | Obligatorio.                                                                                                   |
| [MODELO DE \_ DISPOSITIVO \_ WPD](device-properties.md)                                                          | Obligatorio.                                                                                                   |
| [NÚMERO DE SERIE \_ DEL DISPOSITIVO \_ \_ WPD](device-properties.md)                                         | Obligatorio.                                                                                                   |
| [EL DISPOSITIVO WPD \_ \_ ADMITE \_ DISPOSITIVOS NO \_ CONSUMIBLES](device-properties.md)                    | Obligatorio si el dispositivo admite objetos no consumibles; es decir, si se puede usar para el almacenamiento de datos simple. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Opcional.                                                                                                   |
| [NOMBRE DESCRIPTIVO \_ DEL DISPOSITIVO \_ \_ WPD](device-properties.md)                                         | Se recomienda su uso.                                                                                                |
| [ESQUEMA DRM \_ COMPATIBLE \_ CON \_ DISPOSITIVOS \_ WPD](device-properties.md)                          | Se recomienda si el dispositivo admite Digital Rights Management (DRM).                                         |
| [SE \_ ORDENAN \_ LOS FORMATOS \_ COMPATIBLES CON \_ DISPOSITIVOS \_ WPD](device-properties.md)       | Se recomienda si el dispositivo admite el orden de formato preferido.                                               |
| [TIPO DE \_ DISPOSITIVO \_ WPD](device-properties.md)                                                            | Se recomienda su uso.                                                                                                |
| [IDENTIFICADOR ÚNICO FUNCIONAL \_ \_ DEL DISPOSITIVO \_ \_ WPD](device-properties.md)                          | Opcional.                                                                                                   |
| [IDENTIFICADOR ÚNICO \_ DEL MODELO DE DISPOSITIVO \_ \_ \_ WPD](device-properties.md)                                    | Opcional.                                                                                                   |
| [TRANSPORTE DE \_ \_ DISPOSITIVOS WPD](device-properties.md)                                                  | Se recomienda su uso.                                                                                                |
| [FASE DE \_ USO DEL \_ DISPOSITIVO WPD \_ \_](device-properties.md)                                  | Opcional.                                                                                                   |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](device-properties.md)                             | Obligatorio.                                                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="commands"></a>Comandos

Además de las propiedades, los dispositivos deben admitir un conjunto específico de comandos definidos por Windows portables. Los comandos que admite un objeto o dispositivo dependen de su tipo, funcionalidad y funcionalidades.

En la tabla siguiente se describen las clases de comandos que se aplican a los dispositivos, por funcionalidad. Normalmente, un dispositivo se encuentra en varias categorías y debe admitir los comandos para todas las categorías aplicables. Por ejemplo, un teléfono móvil con una cámara se encuentra en tres categorías: todos los dispositivos, los dispositivos SMS y los dispositivos de captura de imágenes. Un controlador personalizado y una aplicación cliente pueden admitir comandos o propiedades adicionales que defina, pero deben admitir los siguientes comandos. Para obtener una descripción de los comandos específicos que se incluyen en cada categoría de comandos, vea [Comandos](commands.md).



| Descripción                                                                                                                                                                                                                      | Categorías de comandos                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Todos los dispositivos.                                                                                                                                                                                                                     | **CAPACIDADES DE \_ CATEGORÍA \_ WPDWPD \_ CATEGORY \_ COMMON**<br/> **ENUMERACIÓN DE \_ OBJETOS DE \_ CATEGORÍA \_ WPD**<br/> **ADMINISTRACIÓN DE OBJETOS \_ DE CATEGORÍA \_ \_ WPD**<br/> **PROPIEDADES DE OBJETO \_ DE CATEGORÍA \_ \_ WPD**<br/> **PROPIEDADES \_ MASIVAS DE OBJETOS \_ DE \_ CATEGORÍA WPD \_**<br/> **RECURSOS DE OBJETO \_ DE CATEGORÍA \_ \_ WPD**<br/> |
| Dispositivos que pueden capturar imágenes fijas, como cámaras digitales.                                                                                                                                                                  | **CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA \_ DE \_ \_ WPD**                                                                                                                                                                                                                                                                                   |
| Dispositivos que pueden enviar mensajes de servicio de mensajes cortos (SMS), como teléfonos móviles. El envío de mensajes SMS a menudo se denomina "mensajería de texto".                                                                                      | **SMS DE \_ CATEGORÍA \_ WPD**                                                                                                                                                                                                                                                                                                     |
| Dispositivos que funcionan como dispositivos de almacenamiento. Estas incluyen unidades externas. Si un dispositivo admite la capacidad de dar formato a un almacén o mover objetos de una ubicación a otra, el controlador debe admitir esta categoría.<br/> | **ALMACENAMIENTO DE \_ CATEGORÍA \_ WPD**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




