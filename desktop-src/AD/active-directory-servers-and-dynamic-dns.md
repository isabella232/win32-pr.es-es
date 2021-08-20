---
title: Active Directory y DNS dinámico
description: Los Active Directory publican sus direcciones para que los clientes puedan encontrarlos conociendo solo el nombre de dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- dns dinámico Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9508bd571cf60d3801cc5708276ff9399494e354ee3559efd0a3ffa0b96836a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025205"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Active Directory y DNS dinámico

Los Active Directory publican sus direcciones para que los clientes puedan encontrarlos conociendo solo el nombre de dominio. Active Directory los servidores se publican mediante los registros de recursos de servicio (RR de SRV) en DNS. SRV RR es un registro DNS que se usa para asignar el nombre de un servicio a la dirección de un servidor que ofrece el servicio. El nombre de un RR de SRV tiene este formato:


```C++
<service>.<protocol>.<domain>
```



Active Directory servidores ofrecen el servicio LDAP a través del protocolo TCP para que los nombres publicados sean "ldap.tcp.". <domain> Por lo tanto, SRV RR para fabrikam.com es "ldap.tcp.fabrikam.com". Los datos adicionales sobre SRV RR indican la prioridad y el peso del servidor, lo que permite a los clientes elegir el mejor servidor para sus necesidades.

Cuando se Active Directory servidor, usa DNS dinámico para publicarse. Dado que las direcciones TCP/IP están sujetas a cambios, los servidores comprueban periódicamente sus registros para asegurarse de que son correctos y las actualizan si es necesario.

DNS dinámico es una incorporación reciente al estándar DNS. DNS dinámico define un protocolo para actualizar dinámicamente un servidor DNS con nuevos datos. Antes del DNS dinámico, los administradores tenían que configurar manualmente los registros almacenados por los servidores DNS.

 

 




