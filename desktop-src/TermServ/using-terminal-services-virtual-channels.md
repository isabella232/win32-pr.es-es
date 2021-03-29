---
title: Uso de Servicios de Escritorio remoto canales virtuales
description: Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774287"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Uso de Servicios de Escritorio remoto canales virtuales

Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual. El módulo de servidor puede ser una aplicación de modo de usuario o un controlador en modo kernel. El módulo cliente debe ser un archivo DLL.

Para obtener descripciones de estos módulos, vea los temas siguientes.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Aplicación de servidor de canal virtual](virtual-channel-server-application.md)
</dt> <dd>

El módulo de servidor de una aplicación que usa canales virtuales debe ser una aplicación de modo de usuario que se ejecute en una sesión de cliente en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Tenga en cuenta que debe proporcionar un método para iniciar la aplicación de servidor.

</dd> <dt>

[DLL de cliente de canal virtual](virtual-channel-client-dll.md)
</dt> <dd>

El cliente de una aplicación de canales virtuales es un archivo DLL que se carga durante la inicialización del Servicios de Escritorio remoto en el equipo cliente. El archivo DLL debe estar registrado en el equipo cliente.

</dd> <dt>

[Registro de cliente de canal virtual](virtual-channel-client-registration.md)
</dt> <dd>

Debe almacenar el nombre del archivo DLL de cliente en el registro.

</dd> <dt>

[Canales virtuales persistentes de control remoto](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal.

</dd> <dt>

[Canales virtuales dinámicos](dynamic-virtual-channels.md)
</dt> <dd>

Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).

</dd> </dl>

Si ha habilitado la aplicación de un canal virtual en la implementación de Servicios de Escritorio remoto, también puede hacer que la aplicación esté disponible para los equipos cliente que tienen acceso al servidor host de sesión de escritorio remoto por medio del control ActiveX Escritorio remoto. Para obtener más información, vea [usar el control ActiveX escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




