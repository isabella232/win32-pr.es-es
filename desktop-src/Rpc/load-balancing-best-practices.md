---
title: Prácticas recomendadas de equilibrio de carga
description: Prácticas recomendadas de equilibrio de carga
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995476"
---
# <a name="load-balancing-best-practices"></a>Prácticas recomendadas de equilibrio de carga

Se deben seguir varios procedimientos recomendados al instalar y configurar el equilibrio de carga de RPC.

En primer lugar, se debe establecer la seguridad en las llamadas de libras entrantes y salientes. Esto significa que las dos claves del registro de [NoSecurity](configuring-load-balancing.md) opcionales no deben estar presentes o deben establecerse en cero.

En segundo lugar, se debe prestar atención a la solución de equilibrio de carga de front-end que se usa junto con la solución de equilibrio de carga de RPC. Por ejemplo, si el equilibrador de carga de front-end usa el equilibrio de carga de round robin simple, debe existir un número impar de servidores en la granja de servidores. Esto se hace para mitigar la posibilidad de que todas las conexiones se reenvíen y, por lo tanto, el mismo servidor o servidores los prestan servicio.

Por seguridad, suele ser conveniente tener un firewall de control de acceso a los servidores proxy RPC. Si se emplea una solución de Firewall basada en Puerto, los extremos de RPC deben ser estáticos para limitar el número de puertos que se abren en el firewall. En Windows Server 2008 y versiones posteriores de Windows, RPC proporciona un mecanismo para asignar un puerto estático a puntos de conexión dinámicos. Esto se logra a través de los comandos de Firewall netsh de RPC. Un conjunto de comandos de ejemplo para establecer la interfaz lb en el puerto estático de 3010 es:

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

El comando RPC netsh se puede usar para establecer un punto de conexión estático para cualquier interfaz dinámica o estática. Esto resulta útil cuando se restringe el acceso a un equipo que ejecuta una solución de Firewall basada en Puerto. Si se usa la solución de Firewall de Windows, la interfaz RPC puede bloquearse o habilitarse sin tener que asignarla a un puerto específico. Para obtener más información, vea la [Referencia del comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 