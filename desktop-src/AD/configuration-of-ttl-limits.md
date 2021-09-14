---
title: Configuración de límites de TTL
description: Un cliente puede solicitar un valor TTL para una entrada que oscila entre 1 y 31557600 (es decir, de 1 segundo a 1 año).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuración de límites de TTL ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062762"
---
# <a name="configuration-of-ttl-limits"></a>Configuración de límites de TTL

Un cliente puede solicitar un valor TTL para una entrada que oscila entre 1 y 31557600 (es decir, de 1 segundo a 1 año). Los valores de atributo **rangeLower** y **rangeUpper** de la definición **attributeSchema** del **atributo entryTTL** aplicarán este intervalo de valores de atributo. Según RFC 2589, los servidores de directorio no son necesarios para aceptar este valor y podrían devolver un valor TTL diferente al cliente. Los clientes deben poder usar este valor dictado por el servidor como su período de actualización de cliente (CRP), que regulará la frecuencia con la que el cliente necesitará realizar la operación de actualización en la entrada dinámica.

Active Directory Domain Services proporcionar a los administradores la capacidad de configurar los valores de TTL predeterminados y mínimos para un bosque. El valor predeterminado de TTL es lo que se asignará a una entrada dinámica recién creada si no se especifica explícitamente un TTL. El TTL mínimo invalidará cualquier valor de TTL especificado por el cliente que sea inferior al mínimo configurado. No es necesario proporcionar ningún valor TTL máximo configurable porque el valor del atributo **rangeUpper** del objeto **attributeSchema** impondrá un máximo. Permitir a los administradores configurar estos valores les permitirá establecer valores de TTL que aplicarán un tráfico de actualización bajo o, en el otro extremo, proporcionarán un directorio muy actualizado.

Los valores predeterminados de los dos parámetros TTL configurables serán los siguientes:

-   Valor TTL predeterminado = 86400 segundos (1 día)
-   Valor mínimo de TTL = 900 segundos (15 minutos)

Los parámetros de TTL configurables se almacenarán como entradas AVA (aserción de valor de atributo) con el formato " value-name value " en el atributo &lt; &gt; = &lt; &gt; **ms-DS-Other-Configuración** del objeto NTDS-Service especificado por el DN siguiente en la partición De configuración:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



La sintaxis exacta de AVA, para los dos parámetros TTL configurables, es la siguiente, donde NNNN se expresa en segundos:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Un administrador puede establecer estos valores a través de la utilidad de línea de comandos ntdsutil.

 

 




