---
title: Aplicación de servidor de canal virtual
description: El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación en modo de usuario que se ejecute en una sesión de cliente en el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249818"
---
# <a name="virtual-channel-server-application"></a>Aplicación de servidor de canal virtual

El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación en modo de usuario que se ejecute en una sesión de cliente en el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor. Puede hacerlo de varias maneras; Por ejemplo, puede usar un script de inicio de sesión o un programa o script en la carpeta Inicio. Los usuarios también podrían iniciar la aplicación.

Debe almacenar el nombre de la aplicación de servidor de canal virtual en el Registro agregando una subclave en la siguiente ubicación:

**HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminal Server** \\ **Addins**

Para obtener más información sobre la subclave, vea [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).

La aplicación de servidor puede llamar a [**la función WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir un identificador en un canal virtual. A continuación, la aplicación puede usar el identificador en cualquiera de las siguientes funciones.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Cierra un identificador de canal virtual abierto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina todos los datos de entrada en cola enviados desde el cliente al servidor en un canal virtual específico.

> [!Note]  
> Actualmente, esta función no la usa Servicios de Escritorio remoto.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina todos los datos de salida en cola enviados desde el servidor al cliente en un canal virtual específico.

> [!Note]  
> Actualmente, esta función no la usa Servicios de Escritorio remoto.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Devuelve información sobre un canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lee datos del final del servidor de un canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Escribe datos en el final del servidor de un canal virtual.

</dd> </dl>

 

 




