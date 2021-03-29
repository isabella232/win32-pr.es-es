---
title: Aplicación de servidor de canal virtual
description: El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776950"
---
# <a name="virtual-channel-server-application"></a>Aplicación de servidor de canal virtual

El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor. Puede hacerlo de varias maneras: por ejemplo, puede usar un script de inicio de sesión o un programa o script en la carpeta de inicio. Los usuarios también pueden iniciar la aplicación.

Debe almacenar el nombre de la aplicación de servidor de canal virtual en el registro agregando una subclave en la siguiente ubicación:

**HKEY \_ \_** \\  \\  \\ AddIns de **control** \\  \\  del sistema de equipo local Terminal Server

Para obtener más información acerca de la subclave, vea [supervisar conexiones y desconexiones de sesión](monitoring-session-connections-and-disconnections.md).

La aplicación de servidor puede llamar a la función [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir un identificador de un canal virtual. A continuación, la aplicación puede utilizar el identificador en cualquiera de las siguientes funciones.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Cierra un identificador de canal virtual abierto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina todos los datos de entrada en cola enviados del cliente al servidor en un canal virtual específico.

> [!Note]  
> Servicios de Escritorio remoto no usa esta función actualmente.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina todos los datos de salida en cola enviados desde el servidor al cliente en un canal virtual específico.

> [!Note]  
> Servicios de Escritorio remoto no usa esta función actualmente.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Devuelve información sobre un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lee los datos del extremo del servidor de un canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Escribe datos en el extremo del servidor de un canal virtual.

</dd> </dl>

 

 




