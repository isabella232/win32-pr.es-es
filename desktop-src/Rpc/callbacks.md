---
title: Devoluciones de llamada (RPC)
description: A menudo, el modelo de programación requiere una devolución de llamada de servidor a un cliente a través de una llamada a procedimiento remoto (RPC) o llamadas de cliente a un servidor que no es de confianza. Esto presenta muchos problemas potenciales.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078777"
---
# <a name="callbacks-rpc"></a>Devoluciones de llamada (RPC)

A menudo, el modelo de programación requiere una devolución de llamada de servidor a un cliente a través de una llamada a procedimiento remoto (RPC) o llamadas de cliente a un servidor que no es de confianza. Esto presenta muchos problemas potenciales.

En primer lugar, la devolución de llamada al cliente debe realizarse con un nivel de suplantación suficientemente bajo. Si el servidor es un servicio de sistema con privilegios elevados, la devolución de una llamada a un cliente local con un nivel de suplantación de suplantación o superior puede proporcionar al cliente privilegios suficientes para asumir el sistema. Llamar a un cliente remoto con un nivel de suplantación superior al necesario también puede provocar consecuencias no deseadas.

En segundo lugar, si un atacante induce el servicio para realizar una devolución de llamada, puede iniciar lo que se denomina un *agujero negro*: ataque de denegación de servicio. Estos ataques no son específicos de RPC; en estos ataques, un equipo induce que le envíe tráfico, pero no responde a las solicitudes. Puede recibir más recursos y más para llamar al agujero negro, pero nunca vuelven. Un ejemplo genérico de este tipo de ataque es un ataque de nivel TCP denominado ataque de desbordamiento SYN de TCP/IP.

En el nivel de RPC, se produce un ataque de agujero negro simple cuando un atacante llama a una interfaz y solicita al servidor que vuelva a llamar a la interfaz. La interfaz es compatible, pero el atacante nunca devuelve la llamada: un subproceso del servidor está conectado. El atacante realiza esta 100 veces y vincula los subprocesos 100 en el servidor. Finalmente, el servidor se queda sin memoria. La depuración del servidor puede revelar potencialmente la identidad del autor de la llamada de agujero negro, pero a menudo el servidor se reiniciará sin suponer un reinicio de infrecuente, o puede que no haya suficientes conocimientos para determinar el atacante.

El tercer problema está en el cliente. A menudo, un cliente realiza una llamada al servidor que informa al servidor de cómo volver a llamarlo (normalmente un enlace de cadena) y, a continuación, espera a que llegue una llamada del servidor, aceptando ciegamente cualquier llamada en ese punto de conexión que notifica que proceda del servidor. El protocolo de devolución de llamada del servidor al cliente debe incluir algún mecanismo de comprobación para asegurarse de que, cuando llegue la devolución de llamada al cliente, realmente se originó en el servidor.

 

 




