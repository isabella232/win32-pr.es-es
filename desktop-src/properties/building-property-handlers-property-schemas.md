---
description: Las propiedades que se usan en el sistema de propiedades de Windows Vista y versiones posteriores se declaran en los esquemas de propiedades.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Crear propiedades personalizadas.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360928"
---
# <a name="creating-custom-properties"></a>Crear propiedades personalizadas.

Las propiedades que se usan en el sistema de propiedades de Windows Vista y versiones posteriores se declaran en los esquemas de propiedades. Estos esquemas de propiedades se definen en archivos XML y describen diversos aspectos de una propiedad, incluido su tipo (incluida información sobre su tipo primitivo y si es de varios valores), cómo se puede mostrar en la interfaz de usuario de Windows, qué tipo de etiquetas (cadenas de edición descriptivas) se usarán con ella y cómo se almacena en caché en el almacén de búsqueda para obtener un acceso más Las propiedades se identifican por su nombre canónico o su clave de propiedad (PKEY).

Un nombre canónico es el nombre descriptivo del lector de la propiedad y utiliza una Convención de espacio de nombres similar a la que se usa en Microsoft .NET. En el caso de las propiedades definidas por el sistema (las que se incluyen con Windows), la Convención es `System.GroupName.PropertyName` . Tenga en cuenta que el esquema de mayúsculas y minúsculas Pascal, que pone en mayúsculas las letras al principio de cada palabra, se usa en estos nombres. Los nombres canónicos se utilizan en varios lugares, como las listas de propiedades y los nombres de columna en la caché de propiedades. Por lo tanto, se usan en consultas de Lenguaje de consulta estructurado (SQL) para recuperar un valor de propiedad.

Un PKEY es un par de valores que se componen de un GUID y un **valor DWORD**, al que se hace referencia como *formatID* y *propID* , respectivamente. Se representa mediante una estructura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . La mayoría de las API del sistema de propiedades aceptan estas claves de propiedad. El kit de desarrollo de software (SDK) de Windows incluye el archivo de encabezado Propkey. h, que incluye una definición de macro de cada una de las `System` claves de propiedad con la Convención de `PKEY_GroupName_PropertyName` . Por ejemplo, `PKEY_Photo_DateTaken` es la clave de la propiedad de la propiedad con el nombre canónico `System.Photo.DateTaken` . Los valores de propiedad se almacenan en forma de una estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , que es una extensión de los tipos de variante OLE.

Esta sección contiene el tema siguiente, que es integral para crear propiedades personalizadas:

-   [Descripción del esquema de descripción de propiedad](./propdesc-schema-entry.md)

> [!Note]  
> Debido a las posibles dificultades que puede tener el indizador al consumir el esquema del sistema de propiedades, es fundamental que defina los atributos con cuidado y de forma estratégica para la primera versión del esquema. Cualquier cambio en los atributos (tipo, ancho de columna, si indexable) no se reflejará en la base de datos después de que se haya registrado un esquema. Las únicas maneras de que estos cambios se reconozcan después de que el esquema se haya registrado una vez en un sistema serían volver a generar el índice y, a continuación, registrar el nuevo esquema, o registrar el esquema y, a continuación, crear una nueva propiedad para cada versión posterior; por ejemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , y así sucesivamente). No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas extrañas pueden afectar al rendimiento del sistema.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementar controladores de propiedades](./building-property-handlers.md)
</dt> <dt>

[Esquema de descripción de propiedad](./propdesc-schema-entry.md)
</dt> </dl>

 

 
