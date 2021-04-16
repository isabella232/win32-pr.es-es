---
description: Especifica el archivo completo detrás del objeto. También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están incluidos en otros tipos de recursos de dispositivos portátiles de Windows, como un tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546547"
---
# <a name="wpd_resource_default"></a>\_valor predeterminado del recurso WPD \_

Especifica el archivo completo detrás del objeto. También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están incluidos en otros tipos de recursos de dispositivos portátiles de Windows, como un tipo de objeto personalizado.

Se incluirán todos los recursos insertados en el recurso especificado. Por ejemplo, el recurso predeterminado de una carpeta raíz de contactos puede incluir todos los contactos anidados. Sin embargo, no se incluyen los recursos secundarios que simplemente están *vinculados* por metadatos o referencias. Un ejemplo de esto sería una lista de reproducción, que solo podría vincularse a archivos de audio a través de referencias de metadatos o referencias de ruta de texto en el archivo.

El único valor de *PID* permitido para esta **PROPERTYKEY** es cero.

Este tipo de recurso debe admitir los siguientes atributos.



| Nombre del atributo                                                                                                            | Obligatorio u opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ Tamaño total del atributo de recursos de \_ WPD \_](resource-attribute-properties.md)              | Obligatorio.                                              |
| [el \_ atributo del recurso WPD \_ \_ puede \_ leer](attributes.md)                                     | Obligatorio si los clientes pueden leer este recurso.            |
| [el \_ atributo del recurso WPD \_ \_ puede \_ escribir](attributes.md)                                   | Obligatorio si los clientes pueden escribir en este recurso.        |
| [el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar](attributes.md)                                 | Obligatorio si los clientes pueden eliminar este recurso.          |
| [\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD](attributes.md)   | Obligatorio si los clientes tienen acceso de lectura al recurso.  |
| [\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD](attributes.md) | Obligatorio si los clientes tienen acceso de escritura al recurso. |
| [\_formato de \_ atributo de recurso de WPD \_](resource-attribute-properties.md)                       | Obligatorio.                                              |
| [\_clave de \_ recurso de atributo de recurso WPD \_ \_](resource-attribute-properties.md)                                              | Se recomienda su uso.                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Requisitos para recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



