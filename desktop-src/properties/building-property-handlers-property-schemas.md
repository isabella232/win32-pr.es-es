---
description: Las propiedades usadas en el sistema de propiedades de Windows Vista y versiones posteriores se declaran en esquemas de propiedades.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Crear propiedades personalizadas.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263015"
---
# <a name="creating-custom-properties"></a>Crear propiedades personalizadas.

Las propiedades usadas en el sistema de propiedades de Windows Vista y versiones posteriores se declaran en esquemas de propiedades. Estos esquemas de propiedades se definen en archivos XML y describen varios aspectos de una propiedad, incluido su tipo (incluida la información sobre su tipo primitivo y si es multivalor), cómo se puede mostrar en la interfaz de usuario de Windows, qué tipo de etiquetas (cadenas de edición fáciles de usar) se van a usar con él y cómo se almacena en caché en el almacén de búsqueda para un acceso más rápido. Las propiedades se identifican por su nombre canónico o su clave de propiedad (PKEY).

Un nombre canónico es el nombre descriptivo del lector de la propiedad y usa una convención de espacio de nombres similar a la que se usa en Microsoft .NET. Para las propiedades definidas por el sistema (las que se incluyen con Windows), la convención es `System.GroupName.PropertyName` . Tenga en cuenta que el esquema de mayúsculas y minúsculas Pascal, que escribe letras al principio de cada palabra, se usa en estos nombres. Los nombres canónicos se usan en varios lugares, incluidas las listas de propiedades y los nombres de columna en la caché de propiedades. Por lo tanto, se usan Lenguaje de consulta estructurado consultas (SQL) para recuperar un valor de propiedad.

Un PKEY es un par de valores que constan de un GUID y un **DWORD,** a los que se hace referencia como *formatID* y *propID,* respectivamente. Se representa mediante una [**estructura PROPERTYKEY.**](/windows/win32/api/wtypes/ns-wtypes-propertykey) La mayoría de las API del sistema de propiedades aceptan estas claves de propiedad. El kit Windows software (SDK) incluye el archivo de encabezado Propkey.h que incluye una definición de macro de cada una de las claves de propiedad con `System` la convención de `PKEY_GroupName_PropertyName` . Por ejemplo, `PKEY_Photo_DateTaken` es la clave de propiedad de la propiedad con el nombre canónico `System.Photo.DateTaken` . Los valores de propiedad se almacenan en forma de [**una estructura PROPVARIANT,**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) que es una extensión de los tipos OLE VARIANT.

Esta sección contiene el tema siguiente, que es fundamental para crear propiedades personalizadas:

-   [Descripción del esquema de descripción de propiedad](./propdesc-schema-entry.md)

> [!Note]  
> Debido a las posibles dificultades que puede tener el indexador al consumir el esquema del sistema de propiedades, es fundamental definir los atributos de forma cuidadosa y estratégica para la primera versión del esquema. Los cambios en los atributos (tipo, ancho de columna, si se pueden indexar) no se reflejarán en la base de datos después de registrar un esquema. Las únicas maneras de que estos cambios se reconozcan después de registrar el esquema una vez en un sistema sería volver a generar el índice y, a continuación, registrar el nuevo esquema, o registrar el esquema y, a continuación, crear una nueva propiedad para cada versión posterior. por `PKEY_GroupName_PropertyNameV2` ejemplo, `PKEY_GroupName_PropertyNameV3` , , etc.). No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas externas pueden afectar al rendimiento del sistema.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementar controladores de propiedades](./building-property-handlers.md)
</dt> <dt>

[Esquema de descripción de propiedad](./propdesc-schema-entry.md)
</dt> </dl>

 

 
