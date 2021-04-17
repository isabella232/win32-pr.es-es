---
title: Usar una cuenta de usuario de dominio como cuenta de inicio de sesión de servicio
description: Una cuenta de usuario de dominio permite al servicio sacar el máximo partido de las características de seguridad del servicio de Windows y Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: f482359eb8445cacef12c46716ecde662a95d46d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105653288"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Usar una cuenta de usuario de dominio como cuenta de inicio de sesión de servicio

Una cuenta de usuario de dominio permite al servicio sacar el máximo partido de las características de seguridad del servicio de Windows y Microsoft Active Directory Domain Services. El servicio tiene el acceso local y de red que se concede a la cuenta, o a los grupos de los que es miembro la cuenta. El servicio puede admitir la autenticación mutua de Kerberos.

> [!Note]  
> La siguiente documentación es para desarrolladores de. Si es un usuario final que busca información sobre un mensaje de error relacionado con cuentas de usuario de dominio, consulte los foros de la [comunidad de Microsoft](https://answers.microsoft.com). Para obtener información acerca de la administración de cuentas de usuario de dominio, consulte [technet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

La ventaja de usar una cuenta de usuario de dominio es que las acciones del servicio están limitadas por los derechos de acceso y los privilegios asociados a la cuenta. A diferencia de un `LocalSystem` servicio, los errores en un servicio de cuenta de usuario no pueden dañar el sistema. Si el servicio se ve comprometido por un ataque de seguridad, el daño se aísla en las operaciones que el sistema permite que realice la cuenta de usuario. Al mismo tiempo, los clientes que se ejecutan en distintos niveles de privilegios pueden conectarse al servicio, lo que permite al servicio suplantar a un cliente para realizar operaciones confidenciales.

La cuenta de usuario de un servicio no debe ser miembro de los grupos de administradores locales, de dominio o de empresa. Si el servicio necesita privilegios administrativos locales, ejecútelo en la `LocalSystem` cuenta. En el caso de las operaciones que requieren privilegios administrativos de dominio, realizarlas suplantando el contexto de seguridad de una aplicación cliente.

Una instancia de servicio que usa una cuenta de usuario de dominio requiere una acción administrativa periódica para mantener la contraseña de la cuenta. El administrador de control de servicios (SCM) del equipo host de una instancia de servicio almacena en caché la contraseña de la cuenta para utilizarla en el registro en el servicio. Al cambiar la contraseña de la cuenta, también debe actualizar la contraseña almacenada en caché en el equipo host en el que está instalado el servicio. Para obtener más información y un ejemplo de código, consulte [cambiar la contraseña en la cuenta de usuario de un servicio](changing-the-password-on-a-serviceampaposs-user-account.md). Puede evitar el mantenimiento normal si no cambia la contraseña, pero esto aumentaría la probabilidad de que se produzca un ataque de contraseña en la cuenta de servicio. Tenga en cuenta que aunque el SCM almacene la contraseña en una parte segura del registro, está sujeta a ataques.

Una cuenta de usuario de dominio tiene dos formatos de nombre: el nombre distintivo del objeto de usuario en el directorio y el <domain> \\ <username> formato "" usado por el administrador de control de servicios local. Para obtener más información y un ejemplo de código que convierte de un formato a otro, vea [convertir los formatos de nombre de cuenta de dominio](converting-domain-account-name-formats.md).

 

 
