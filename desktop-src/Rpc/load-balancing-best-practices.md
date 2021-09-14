---
title: Procedimientos recomendados de equilibrio de carga
description: Procedimientos recomendados de equilibrio de carga
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244527"
---
# <a name="load-balancing-best-practices"></a>Procedimientos recomendados de equilibrio de carga

Se deben seguir varios procedimientos recomendados al configurar y configurar el equilibrio de carga de RPC.

En primer lugar, se debe establecer la seguridad en las llamadas LBS entrantes y salientes. Esto significa que ambas claves opcionales del Registro [NoSecurity](configuring-load-balancing.md) no deben estar presentes o deben establecerse en cero.

En segundo lugar, se debe prestar atención a la solución de equilibrio de carga front-end que se usa junto con la solución de equilibrio de carga de RPC. Por ejemplo, si el equilibrador de carga front-end usa un equilibrio round robin carga simple, debe existir un número impar de servidores en la granja de servidores. Esto es para mitigar la posibilidad de que todas las conexiones sean reenviadas y, por tanto, atendidas por el mismo servidor o servidor.

Por motivos de seguridad, normalmente es conveniente tener un firewall que controle el acceso a los servidores proxy RPC. Si se emplea una solución de firewall basada en puertos, los puntos de conexión RPC deben ser estáticos para limitar el número de puertos que se abren en el firewall. En Windows Server 2008 y versiones posteriores de Windows, RPC proporciona un mecanismo para asignar un puerto estático a puntos de conexión dinámicos. Esto se logra a través de los comandos de firewall netsh de RPC. Un conjunto de comandos de ejemplo para establecer la interfaz LBS en el puerto estático de 3010 es:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

El comando netsh rpc se puede usar para establecer un punto de conexión estático para cualquier interfaz dinámica o estática. Esto resulta útil al restringir el acceso a una máquina que ejecuta una solución de firewall basada en puertos. Si se Windows solución de firewall, la interfaz RPC se puede bloquear o habilitar sin tener que asignarla a un puerto específico. Para más información, consulte la referencia [de comandos del firewall de netsh RPC.](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10))

 

 