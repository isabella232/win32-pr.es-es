---
description: Explica las estrategias para acceder a los recursos de red.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Acceso de cliente a recursos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8886f474876080703d190efb3419d099027f24af17dd735736957452318e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783081"
---
# <a name="client-access-to-network-resources"></a>Acceso de cliente a recursos de red

Un servidor puede usar las siguientes estrategias para acceder a los recursos de red:

-   Si el servidor tiene el nombre de cuenta y la contraseña de un [](/windows/desktop/SecGloss/c-gly) cliente, puede llamar a [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con las credenciales del cliente para asignar una letra de unidad local a un recurso compartido de red.
-   Después de [**llamar a LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) con credenciales de cliente, el servidor puede llamar a la [**función CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para [crear un proceso para el cliente](processes-in-the-client-security-context.md). Este nuevo proceso de cliente puede acceder a los recursos de red mediante el contexto de [*seguridad del cliente.*](/windows/desktop/SecGloss/s-gly) Por ejemplo, el proceso puede llamar a la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un archivo en un equipo remoto. El sistema usa el token principal del cliente [*para*](/windows/desktop/SecGloss/p-gly) comprobar los intentos de acceso del proceso de cliente.
-   Un servidor puede llamar a [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con credenciales null para establecer una conexión a un recurso de red con acceso al servidor o una conexión predeterminada. Si el servidor se ejecuta como la cuenta LocalSystem, se autentica en el recurso de red en el contexto [*de seguridad*](/windows/desktop/SecGloss/s-gly) del servidor de dominio. Si el servidor se ejecuta con una cuenta de servicio, se autentica como esa cuenta. Para obtener más información, vea [LocalSystem Account](/windows/desktop/Services/localsystem-account).

Para obtener información sobre cómo proteger contraseñas, vea [Control de contraseñas.](/windows/desktop/SecBP/handling-passwords) Para obtener información sobre la adquisición de credenciales, vea [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
