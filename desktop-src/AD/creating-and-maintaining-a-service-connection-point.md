---
title: Crear y mantener un punto de conexión de servicio
description: Al publicar con un SCP, recuerde que debe contener los datos actuales sobre la instancia de servicio.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Creación y mantenimiento de un punto de conexión de servicio AD
- punto de conexión de servicio AD, creación y mantenimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077541"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>Crear y mantener un punto de conexión de servicio

Al publicar con un SCP, recuerde que debe contener los datos actuales sobre la instancia de servicio. De lo contrario, los clientes que se enlazan al SCP recuperan datos obsoletos. El instalador del servicio, que crea un SCP, especifica los valores iniciales para los atributos de los SCP. A continuación, cuando se inicia la instancia de servicio, debe buscar el SCP y actualizar los valores de atributo, si es necesario. De esta manera, los clientes están seguros de los datos más actuales.

Después de crear el SCP, el instalador del servicio realiza dos pasos adicionales que permiten al servicio actualizar el SCP:

-   Establezca ACE en el descriptor de seguridad del objeto SCP para permitir que el servicio modifique los atributos SCP en tiempo de ejecución. Para obtener más información y un ejemplo de código, consulte [habilitación de la cuenta de servicio para acceder a las propiedades de SCP](enabling-service-account-to-access-scp-properties.md).
-   Almacene en caché el **objectGUID** del SCP en el registro del equipo host del servicio. El servicio recupera el GUID almacenado en caché que se va a enlazar al SCP para comprobar y actualizar sus atributos.

El instalador del servicio almacena en caché el **objectGUID** del SCP en lugar de su DN. **ObjectGUID** nunca cambia, independientemente de si se mueve o se cambia el nombre del SCP. El DN puede cambiar si un administrador mueve o cambia el nombre del SCP. Por ejemplo, si crea un SCP como un elemento secundario de un objeto de equipo, el nombre distintivo del SCP cambia si se cambia el nombre del equipo o se mueve a otro dominio o unidad organizativa.

Cuando un instalador de servicio crea un SCP, debe leer el **objectGUID** del objeto recién creado y almacenarlo en caché en el registro del equipo host del servicio. Use el método [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) para obtener el valor **objectGUID** en formato de cadena adecuado para el enlace. Almacene en caché la cadena de GUID como un valor en la siguiente clave del registro.

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

Donde "Vendor name" y "Product Name" identifican el proveedor y el producto.

Cuando se inicia el servicio, recupera la cadena de GUID en caché del registro y la usa para enlazar con el SCP. El servicio Lee los atributos de SCP importantes y los compara con los valores actuales. Si los valores de SCP no están actualizados, el servicio los actualiza. Los valores que el servicio puede necesitar para actualizar incluyen **palabras clave**, **serviceBindingInformation**, **serviceDNSName** y **serviceDNSNameType**.

## <a name="examples"></a>Ejemplos

-   [Ejemplos de scripts](script-samples-for-managing-service-connection-points.md)
-   [Ejemplos de código (C/C++)](code-samples-for-managing-service-connection-points.md)

 

 