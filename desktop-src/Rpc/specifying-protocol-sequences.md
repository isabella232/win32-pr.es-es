---
title: Especificar secuencias de protocolo
description: Las aplicaciones de servidor deben seleccionar una o varias secuencias de protocolo para usarlas al comunicarse con el cliente a través de la red. La elección de secuencias de protocolo depende de la red. Vea Interpretación de la información de enlace y Selección de una secuencia de protocolo.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a700299e3d2bd98fa5fb0aaebea25e907d85afb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473509"
---
# <a name="specifying-protocol-sequences"></a>Especificar secuencias de protocolo

Las aplicaciones de servidor deben seleccionar una o varias secuencias de protocolo para usarlas al comunicarse con el cliente a través de la red. La elección de secuencias de protocolo depende de la red. Vea [Interpretación de la información de enlace](interpreting-binding-information.md) y Selección de una secuencia de [protocolo.](selecting-a-protocol-sequence.md)

El programa de servidor puede permitir que los clientes se conecten mediante cualquier secuencia de protocolo que admita la red. Para ello, [**invoque RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) y pase RPC \_ C \_ PROTSEQ \_ MAX \_ REQS \_ DEFAULT como primer parámetro. Sin embargo, este no es el enfoque recomendado. En su lugar, el **uso de ncalrpc para** llamadas locales y **ncacn \_ ip \_ tcp** o **ncacn \_ http** para llamadas remotas suele ser suficiente. Las redes heterogéneos son poco frecuentes y prácticamente todas las redes admiten TCP/IP.

Si desea que el cliente restrinja la asignación de puertos para los puntos de conexión dinámicos a un intervalo de puertos específico, llame a [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) en su lugar. Esta función es específica de RPC de Microsoft y es muy útil para las llamadas a procedimientos remotos que pasan a través de un firewall. Usa un parámetro adicional para pasar marcas de control de asignación de puertos a la función. Vea [Configuring the Registry for Port Allocations and Selective Binding](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

Puede especificar secuencias de protocolo e información de punto de conexión en el archivo MIDL al desarrollar las interfaces del servidor. Si lo hace, el servidor debe usar [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) para registrar todas las secuencias de protocolo y la información de punto de conexión asociada proporcionada en el archivo IDL. Además, hay una función [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) correspondiente que también permite al servidor pasar marcas de control y asignación de puertos.

Si desea configurar los programas de cliente y servidor para que se comuniquen con una secuencia de protocolo especificada, la aplicación de servidor debe llamar a [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Para obtener una lista completa de las secuencias de protocolo RPC de Microsoft, vea [Constantes de secuencia de protocolo .](protocol-sequence-constants.md)

Rpc de Microsoft también proporciona [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) para permitir que las aplicaciones seleccionen secuencias de protocolo específicas y controlen la asignación dinámica de puertos.

Además de los protocolos orientados a conexiones, Rpc de Microsoft también admite protocolos de datagramas (sin conexión). Se recomiendan los protocolos orientados a la conexión; Los protocolos de datagramas tienen conjuntos de características diferentes a los protocolos orientados a la conexión y solo se deben usar si un desarrollador de sistemas distribuidos requiere una característica disponible solo en protocolos de datagramas. Algunas de las características disponibles al usar protocolos de datagramas son:

-   Los datagramas admiten los protocolos de transporte sin conexión UDP e IPX.
-   Dado que no es necesario establecer y mantener una conexión, el protocolo RPC del datagrama requiere menos sobrecarga de recursos.
-   Los datagramas permiten un enlace más rápido.
-   Al igual que con RPC orientado a la conexión, las llamadas RPC de datagramas son de forma predeterminada *no inempotentes.* Esto significa que se garantiza que la llamada no se ejecutará más de una vez. Sin embargo, una función se puede marcar como idempotente en el archivo IDL que le dice a RPC que es inofensivo ejecutar la función más de una vez en respuesta a una única solicitud de cliente. Esto permite que el tiempo de ejecución mantenga menos estado en el servidor. Tenga en cuenta que una llamada idempotente se volvería a ejecutar solo en raras circunstancias en una red inestable.
-   RPC de datagrama admite el [atributo IDL](/windows/desktop/Midl/broadcast) de difusión. La difusión permite a un cliente emitir mensajes a varios servidores al mismo tiempo. Esto permite al cliente localizar uno de los varios servidores disponibles en la red o controlar varios servidores simultáneamente. Tenga en cuenta que la difusión del datagrama solo es válida dentro del vínculo local y normalmente no cruza los enrutadores. Las llamadas de difusión son idempotentes implícitamente. Si la llamada contiene \[ **parámetros out,** solo se devuelve la \] primera respuesta del servidor. Una vez que un servidor responda, todos los RPC futuros sobre ese identificador de enlace solo se enviarán a ese servidor, incluidas las llamadas con el atributo de difusión. Para enviar otra difusión, cree un nuevo identificador de enlace o llame a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) en el identificador existente.
-   RPC de datagrama admite [el atributo](/windows/desktop/Midl/maybe) quizás IDL. Esto permite al cliente enviar una llamada al servidor sin esperar una respuesta o confirmación. La llamada no puede contener \[ **parámetros** \] out. Las llamadas que usan **\[ quizás \]** las llamadas son idempotentes implícitamente.

 

 