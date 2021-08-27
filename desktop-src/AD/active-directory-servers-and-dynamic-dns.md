---
title: Active Directory y DNS dinámico
description: Los Active Directory publican sus direcciones para que los clientes puedan encontrarlos sabiendo solo el nombre de dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- dns dinámico Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9828a2d6d14d862e98d3c5c4129bbc70f5c411
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880070"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Active Directory y DNS dinámico

Los Active Directory publican sus direcciones para que los clientes puedan encontrarlos sabiendo solo el nombre de dominio. Active Directory los servidores se publican mediante los registros de recursos de servicio (RR de SRV) en DNS. SRV RR es un registro DNS que se usa para asignar el nombre de un servicio a la dirección de un servidor que ofrece el servicio. El nombre de un RR de SRV tiene este formato:


```C++
<service>.<protocol>.<domain>
```



Active Directory servidores ofrecen el servicio LDAP a través del protocolo TCP para que los nombres publicados sean "ldap.tcp. &lt; dominio &gt; ". Por lo tanto, el RR de SRV fabrikam.com es "ldap.tcp.fabrikam.com". Los datos adicionales sobre SRV RR indican la prioridad y el peso del servidor, lo que permite a los clientes elegir el mejor servidor para sus necesidades.

Cuando se Active Directory servidor de aplicaciones, usa DNS dinámico para publicarse a sí mismo. Dado que las direcciones TCP/IP están sujetas a cambios, los servidores comprueban periódicamente sus registros para asegurarse de que son correctos y los actualizan si es necesario.

EL DNS dinámico es una incorporación reciente al estándar DNS. DNS dinámico define un protocolo para actualizar dinámicamente un servidor DNS con nuevos datos. Antes de DNS dinámico, los administradores tenían que configurar manualmente los registros almacenados por los servidores DNS.

 

 




