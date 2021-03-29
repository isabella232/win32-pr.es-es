---
title: Servidores de Active Directory y DNS dinámico
description: Los servidores Active Directory publican sus direcciones de modo que los clientes puedan encontrarlos sabiendo solo el nombre de dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772757"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Servidores de Active Directory y DNS dinámico

Los servidores Active Directory publican sus direcciones de modo que los clientes puedan encontrarlos sabiendo solo el nombre de dominio. Los servidores Active Directory se publican mediante los registros de recursos de servicio (RR de SRV) en DNS. SRV RR es un registro DNS que se usa para asignar el nombre de un servicio a la dirección de un servidor que ofrece el servicio. El nombre de un RR SRV tiene este formato:


```C++
<service>.<protocol>.<domain>
```



Los servidores Active Directory ofrecen el servicio LDAP a través del protocolo TCP para que los nombres publicados sean "LDAP. TCP. <domain> ". Por lo tanto, el RR SRV para fabrikam.com es "ldap.tcp.fabrikam.com". Los datos adicionales sobre el RR SRV indican la prioridad y el peso del servidor, lo que permite a los clientes elegir el mejor servidor para sus necesidades.

Cuando se instala un servidor de Active Directory, utiliza DNS dinámico para publicarse. Dado que las direcciones TCP/IP están sujetas a cambios, los servidores comprueban periódicamente sus registros para asegurarse de que son correctos y los actualizan si es necesario.

DNS dinámico es una adición reciente al estándar DNS. DNS dinámico define un protocolo para actualizar dinámicamente un servidor DNS con nuevos datos. Antes del DNS dinámico, los administradores tenían que configurar manualmente los registros almacenados por los servidores DNS.

 

 




