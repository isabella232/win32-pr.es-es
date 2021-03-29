---
title: Configuración de límites de TTL
description: Un cliente puede solicitar un valor de TTL para una entrada comprendida entre 1 y 31557600 (es decir, de 1 segundo a 1 año).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuración de límites de TTL de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772732"
---
# <a name="configuration-of-ttl-limits"></a>Configuración de límites de TTL

Un cliente puede solicitar un valor de TTL para una entrada comprendida entre 1 y 31557600 (es decir, de 1 segundo a 1 año). Los valores del atributo **rangeLower** y **rangeUpper** aplicarán este intervalo de valores de atributo en la definición de **attributeSchema** para el atributo **entryTTL** . Según RFC 2589, no es necesario que los servidores de directorio acepten este valor y que devuelvan un valor de TTL diferente al cliente. Los clientes deben poder usar este valor dictado por el servidor como período de actualización del cliente (CRP), que regirá la frecuencia con la que el cliente necesitará realizar la operación de actualización en la entrada dinámica.

Active Directory Domain Services proporcionar a los administradores la capacidad de configurar los valores predeterminados y mínimos de TTL para un bosque. El valor TTL predeterminado es lo que se asignará a una entrada dinámica recién creada si no se especifica un TTL explícitamente. El TTL mínimo invalidará cualquier valor de TTL especificado por el cliente inferior al mínimo configurado. No se debe proporcionar ningún valor TTL máximo configurable porque el valor del atributo **rangeUpper** del objeto **attributeSchema** impondrá un máximo. Permitir a los administradores configurar estos valores les permitirá establecer valores de TTL que aplicarán un tráfico de poca actualización o, en el otro extremo, proporcionarán un directorio muy actualizado.

Los valores predeterminados para los dos parámetros de TTL configurables serán los siguientes:

-   Valor TTL predeterminado = 86400 segundos (1 día)
-   Valor TTL mínimo = 900 segundos (15 minutos)

Los parámetros de TTL que se pueden configurar se almacenarán como entradas de AVA (aserción de valor de atributo) con el formato "<nombre-valor>=<value>"en el atributo **MS-DS-Other-Settings** del objeto NTDS-Service proporcionado por el DN siguiente en la partición de configuración:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



La sintaxis exacta de AVA, para los dos parámetros de TTL configurables, es la siguiente, donde NNNN se expresa en segundos:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Los administradores pueden establecer estos valores a través de la utilidad de línea de comandos Ntdsutil.

 

 




