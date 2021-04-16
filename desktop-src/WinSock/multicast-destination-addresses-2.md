---
description: Cuando se envía a una dirección de destino de multidifusión, el protocolo IPv6 de Microsoft requiere normalmente que la aplicación tenga una interfaz de salida especificada.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Direcciones IPv6 de destino de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497453"
---
# <a name="ipv6-multicast-destination-addresses"></a>Direcciones IPv6 de destino de multidifusión

Cuando se envía a una dirección de destino de multidifusión, el protocolo IPv6 de Microsoft requiere normalmente que la aplicación tenga una interfaz de salida especificada. Esto se hace con la opción de socket de **\_ multidifusión IPv6 \_ si** se enlaza el socket a una dirección de origen específica.

También puede especificar una interfaz predeterminada para una dirección de multidifusión específica, un ámbito de dirección de multidifusión completo o todas las direcciones de multidifusión. Esto se hace con una ruta que coloca el prefijo de multidifusión en el vínculo a la interfaz de salida deseada. En los siguientes ejemplos se muestra cómo se puede especificar esto:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



