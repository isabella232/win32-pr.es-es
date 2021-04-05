---
title: Terminología de enlace RPC esencial
description: Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los siguientes términos.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- RPC llamada a procedimiento remoto, descripción, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078202"
---
# <a name="essential-rpc-binding-terminology"></a>Terminología de enlace RPC esencial

Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los siguientes términos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Secuencia de protocolos
</dt> <dd>

Cuando los sistemas operativos de red se comunican entre sí, deben escuchar y hablar del mismo idioma. Estos idiomas se denominan *secuencias de protocolo*. Los programas de cliente y servidor deben usar secuencias de protocolo que admita la red que los conecta. Microsoft RPC admite una variedad de secuencias de protocolos. Para obtener más información, consulte [seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md), [especificar secuencias de protocolos](specifying-protocol-sequences.md)y [**punto de conexión**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Equipo host del servidor o sistema host del servidor
</dt> <dd>

El programa de servidor se ejecuta en el equipo host del servidor. Sin embargo, en muchos casos, la informática cliente/servidor hace referencia tanto al programa de servidor como al equipo host del servidor como "servidor". El resultado es que no siempre es evidente lo que se está analizando.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales
</dt> <dd>

Los programas de servidor escuchan un puerto o un grupo de puertos en el equipo host del servidor para las solicitudes de cliente. Los sistemas host de servidor mantienen una base de datos de estos puertos, que se denominan puntos de conexión en RPC. La base de datos se denomina asignación de puntos de conexión.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Enlace
</dt> <dd>

Los programas cliente crean un enlace con el servidor para establecer una sesión de comunicación. Un enlace contiene toda la información que las aplicaciones cliente necesitan para crear la sesión.

</dd> </dl>

 

 