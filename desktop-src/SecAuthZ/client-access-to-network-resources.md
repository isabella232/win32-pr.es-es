---
description: Explica las estrategias para tener acceso a los recursos de red.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Acceso de cliente a los recursos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648236"
---
# <a name="client-access-to-network-resources"></a>Acceso de cliente a los recursos de red

Un servidor puede utilizar las siguientes estrategias para tener acceso a los recursos de red:

-   Si el servidor tiene el nombre de cuenta y la contraseña de un cliente, puede llamar a [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con las [*credenciales*](/windows/desktop/SecGloss/c-gly) del cliente para asignar una letra de unidad local a un recurso compartido de red.
-   Después de llamar a [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) con las credenciales de cliente, el servidor puede llamar a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para [crear un proceso para el cliente](processes-in-the-client-security-context.md). Este nuevo proceso de cliente puede tener acceso a los recursos de red mediante el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly)del cliente. Por ejemplo, el proceso puede llamar a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un archivo en un equipo remoto. El sistema utiliza el [*token principal*](/windows/desktop/SecGloss/p-gly) del cliente para comprobar los intentos de acceso por parte del proceso del cliente.
-   Un servidor puede llamar a [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) con credenciales nulas para establecer una conexión a un recurso de red con acceso al servidor o una conexión predeterminada. Si el servidor se ejecuta como la cuenta LocalSystem, se autentica en el recurso de red en el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) del servidor de dominio. Si el servidor se ejecuta con una cuenta de servicio, se autentica como esa cuenta. Para obtener más información, consulte la [cuenta LocalSystem](/windows/desktop/Services/localsystem-account).

Para obtener información sobre cómo proteger las contraseñas, consulte [Administrar contraseñas](/windows/desktop/SecBP/handling-passwords). Para obtener información acerca de la adquisición de credenciales, consulte [solicitar credenciales al usuario](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
