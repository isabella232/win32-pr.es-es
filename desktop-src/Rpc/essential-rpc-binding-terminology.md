---
title: Terminología esencial del enlace RPC
description: Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los términos siguientes.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Llamada a procedimiento remoto RPC, descrita, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08b0741b27360fe81c2ed713ee39189ef043073c03bc7e12d53165f8a09146c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021445"
---
# <a name="essential-rpc-binding-terminology"></a>Terminología esencial del enlace RPC

Para ayudar mejor en una explicación del proceso de conexión de cliente/servidor, es útil conocer los términos siguientes.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Secuencia de protocolo
</dt> <dd>

Cuando los sistemas operativos de red se comunican entre sí, deben escuchar y hablar el mismo idioma. Estos lenguajes se *denominan secuencias de protocolo.* Los programas de cliente y servidor deben usar secuencias de protocolo que admita la red que los conecta. Rpc de Microsoft admite una variedad de secuencias de protocolo. Para obtener más información, [vea Seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md), Especificar [secuencias de protocolo y](specifying-protocol-sequences.md)punto de [**conexión**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Equipo host de servidor o sistema host de servidor
</dt> <dd>

El programa de servidor se ejecuta en el equipo host del servidor. Sin embargo, mucha documentación sobre la informática cliente/servidor hace referencia tanto al programa de servidor como al equipo host del servidor como "servidor". El resultado es que no siempre está claro qué se está analizando.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremo
</dt> <dd>

Los programas de servidor escuchan un puerto o un grupo de puertos en el equipo host del servidor para las solicitudes de cliente. Los sistemas host de servidor mantienen una base de datos de estos puertos, que se denominan puntos de conexión en RPC. La base de datos se denomina mapa de punto de conexión.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Vinculante
</dt> <dd>

Los programas cliente crean un enlace al servidor para establecer una sesión de comunicación. Un enlace contiene toda la información que las aplicaciones cliente necesitan para crear la sesión.

</dd> </dl>

 

 