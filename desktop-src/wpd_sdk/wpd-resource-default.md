---
description: Especifica el archivo completo detrás del objeto . También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están cubiertos por otros tipos de recursos Windows dispositivos portátiles, como un tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360916"
---
# <a name="wpd_resource_default"></a>WPD \_ RESOURCE \_ DEFAULT

Especifica el archivo completo detrás del objeto . También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están cubiertos por otros tipos de recursos Windows dispositivos portátiles, como un tipo de objeto personalizado.

Se incluirán todos los recursos insertados en el recurso especificado. Por ejemplo, el recurso predeterminado de una carpeta raíz de contactos puede incluir todos los contactos anidados. Sin embargo, no se incluyen los recursos secundarios que simplemente están *vinculados* por metadatos o referencias. Un ejemplo de esto sería una lista de reproducción, que solo podría vincular a archivos de audio a través de referencias de metadatos o referencias de ruta de acceso textuales en el archivo.

El único valor *pid permitido* para **este PROPERTYKEY** es cero.

Este tipo de recurso debe admitir los atributos siguientes.



| Nombre del atributo                                                                                                            | Obligatorio u opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [TAMAÑO TOTAL DEL \_ ATRIBUTO \_ DE RECURSO \_ \_ WPD](resource-attribute-properties.md)              | Necesario.                                              |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ LEER](attributes.md)                                     | Obligatorio si los clientes pueden leer este recurso.            |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ESCRIBIR](attributes.md)                                   | Obligatorio si los clientes pueden escribir en este recurso.        |
| [EL ATRIBUTO \_ DE RECURSO WPD \_ PUEDE \_ \_ ELIMINAR](attributes.md)                                 | Obligatorio si los clientes pueden eliminar este recurso.          |
| [TAMAÑO ÓPTIMO DEL BÚFER DE LECTURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD](attributes.md)   | Obligatorio si los clientes tienen acceso de lectura al recurso.  |
| [TAMAÑO ÓPTIMO DEL BÚFER DE ESCRITURA \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ \_ \_ WPD](attributes.md) | Obligatorio si los clientes tienen acceso de escritura al recurso. |
| [FORMATO DE ATRIBUTO \_ DE \_ RECURSO \_ WPD](resource-attribute-properties.md)                       | Necesario.                                              |
| [CLAVE DE RECURSO \_ DEL ATRIBUTO DE RECURSO \_ \_ \_ WPD](resource-attribute-properties.md)                                              | Se recomienda su uso.                                           |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Requisitos de recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



