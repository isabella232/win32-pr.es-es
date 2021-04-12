---
title: Especificar secuencias de protocolo
description: Las aplicaciones de servidor deben seleccionar una o más secuencias de protocolo para usarlas al comunicarse con el cliente a través de la red. La elección de las secuencias de protocolo depende de la red. Consulte interpretar la información de enlace y seleccionar una secuencia de protocolo.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a700299e3d2bd98fa5fb0aaebea25e907d85afb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359226"
---
# <a name="specifying-protocol-sequences"></a>Especificar secuencias de protocolo

Las aplicaciones de servidor deben seleccionar una o más secuencias de protocolo para usarlas al comunicarse con el cliente a través de la red. La elección de las secuencias de protocolo depende de la red. Consulte [interpretar la información de enlace](interpreting-binding-information.md) y [seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md).

El programa de servidor puede permitir que los clientes se conecten mediante cualquier secuencia de protocolos que admita la red. Para ello, invoque [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) y pase \_ \_ \_ el valor predeterminado de los requisitos máximos de RPC C PROTSEQ Max \_ \_ como primer parámetro. Sin embargo, no es el enfoque recomendado. En su lugar, el uso de **ncalrpc** para llamadas locales y **ncacn \_ IP \_ TCP** o **ncacn \_ http** para llamadas remotas suele ser suficiente. Las redes heterogéneas no son frecuentes y prácticamente todas las redes admiten TCP/IP.

Si desea que el cliente restrinja la asignación de puertos para los puntos de conexión dinámicos a un intervalo de puertos específico, llame a [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) en su lugar. Esta función es específica de Microsoft RPC y es muy útil para las llamadas a procedimientos remotos que pasan a través de un firewall. Usa un parámetro adicional para pasar las marcas de control de asignación de puerto a la función. Vea [configurar el registro para asignaciones de puerto y enlace selectivo](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

Puede especificar secuencias de protocolos e información de extremo en el archivo MIDL cuando desarrolle las interfaces del servidor. Si lo hace, el servidor debe usar [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) para registrar todas las secuencias de protocolo y la información de punto de conexión asociada proporcionada en el archivo IDL. Además, hay una función [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) correspondiente que también permite al servidor pasar las marcas de asignación de puertos.

Si desea configurar los programas de cliente y servidor para que se comuniquen con una secuencia de protocolo especificada, la aplicación de servidor debe llamar a [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Para obtener una lista completa de las secuencias de protocolo RPC de Microsoft, vea [constantes de secuencia de protocolos](protocol-sequence-constants.md).

Microsoft RPC también proporciona [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) para permitir que las aplicaciones seleccionen secuencias de protocolo específicas y controlen la asignación dinámica de puertos.

Además de los protocolos orientados a la conexión, Microsoft RPC es compatible también con los protocolos de datagramas (sin conexión). Se recomiendan los protocolos orientados a la conexión; los protocolos de datagrama tienen diferentes conjuntos de características que los protocolos orientados a la conexión y solo se deben usar si un programador del sistema distribuido requiere una característica disponible únicamente en los protocolos de datagramas. Algunas de las características disponibles cuando se usan protocolos de datagrama son:

-   Los datagramas admiten los protocolos de transporte UDP e IPX sin conexión.
-   Dado que no es necesario establecer y mantener una conexión, el protocolo RPC de datagrama requiere menos sobrecarga de recursos.
-   Los datagramas permiten un enlace más rápido.
-   Al igual que con RPC orientado a la conexión, las llamadas RPC de datagrama son de forma predeterminada *nonidempotent*. Esto significa que se garantiza que la llamada no se ejecute más de una vez. Sin embargo, una función puede marcarse como idempotente en el archivo IDL que indica a RPC que es inofensivo ejecutar la función más de una vez como respuesta a una única solicitud de cliente. Esto permite que el tiempo de ejecución mantenga menos estado en el servidor. Tenga en cuenta que una llamada idempotente se volverá a ejecutar solo en raras circunstancias en una red inestable.
-   Datagrama RPC admite el atributo IDL de [difusión](/windows/desktop/Midl/broadcast) . La difusión permite a un cliente emitir mensajes a varios servidores al mismo tiempo. Esto permite al cliente localizar uno de varios servidores disponibles en la red o controlar varios servidores simultáneamente. Tenga en cuenta que la difusión del datagrama solo es válida dentro del vínculo local y normalmente no cruza los enrutadores. Las llamadas de difusión son implícitamente idempotente. Si la llamada contiene \[ parámetros **out** \] , solo se devuelve la primera respuesta del servidor. Una vez que un servidor responde, todas las RPC futuras sobre ese identificador de enlace se enviarán solo a ese servidor, incluidas las llamadas con el atributo de difusión. Para enviar otra difusión, cree un nuevo identificador de enlace o llame a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) en el identificador existente.
-   El datagrama RPC admite el atributo [puede](/windows/desktop/Midl/maybe) ser IDL. Esto permite al cliente enviar una llamada al servidor sin tener que esperar una respuesta o una confirmación. La llamada no puede contener \[  \] parámetros out. Las llamadas que usan las llamadas **\[ quizás \]** son implícitamente idempotente.

 

 