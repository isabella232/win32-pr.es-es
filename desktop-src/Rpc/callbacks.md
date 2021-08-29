---
title: Devoluciones de llamada (RPC)
description: A menudo, el modelo de programación requiere una devolución de llamada de servidor a un cliente a través de una llamada a procedimiento remoto (RPC) o llamadas de cliente a un servidor que no es de confianza. Esto presenta muchos posibles problemas.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe19db092885e745d8dd97c8b0e034f2230327b9a2327417dc73d834940762e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022945"
---
# <a name="callbacks-rpc"></a>Devoluciones de llamada (RPC)

A menudo, el modelo de programación requiere una devolución de llamada de servidor a un cliente a través de una llamada a procedimiento remoto (RPC) o llamadas de cliente a un servidor que no es de confianza. Esto presenta muchos posibles problemas.

En primer lugar, la devolución de llamada al cliente debe realizarse con un nivel de suplantación lo suficientemente bajo. Si el servidor es un servicio de sistema con privilegios elevados, la llamada a un cliente local con un nivel de suplantación de suplantación o superior puede proporcionar al cliente privilegios suficientes para asumir el control del sistema. La llamada a un cliente remoto con un nivel de suplantación mayor del necesario también puede provocar consecuencias no deseadas.

En segundo lugar, si un atacante induce a su servicio a realizar una devolución de llamada, puede iniciar lo que se denomina un hueco *negro:* ataque por denegación de servicio. Estos ataques no son específicos de RPC; en estos ataques, una máquina le induce a enviarle tráfico, pero no responde a sus solicitudes. Se receptora cada vez más recursos para llamar al hueco negro, pero nunca volverán. Un ejemplo genérico de este tipo de ataque es un ataque de nivel TCP denominado ataque de desbordamiento SYN de TCP/IP.

En el nivel RPC, se produce un ataque simple de "black-hole" cuando un atacante llama a una interfaz y solicita al servidor que vuelva a llamar a la interfaz. La interfaz cumple, pero el atacante nunca devuelve la llamada: un subproceso en el servidor está vinculado. El atacante lo hace 100 veces y asocia 100 subprocesos en el servidor. Finalmente, el servidor se queda sin memoria. La depuración del servidor puede revelar potencialmente la identidad del autor de la llamada, pero a menudo el servidor se reiniciará sin sospecha de juego desenlazar, o puede que no haya suficiente experiencia disponible para determinar el atacante.

El tercer obstáculo está en el cliente. A menudo, un cliente realiza una llamada al servidor que informa al servidor de cómo llamarlo (normalmente un enlace de cadena) y, a continuación, espera a que llegue una llamada del servidor, aceptando a la vista cualquier llamada en ese punto de conexión que dice que procede del servidor. El protocolo de devolución de llamada del servidor al cliente debe incluir algún mecanismo de comprobación para asegurarse de que, cuando la devolución de llamada llega al cliente, se origina realmente en el servidor.

 

 




