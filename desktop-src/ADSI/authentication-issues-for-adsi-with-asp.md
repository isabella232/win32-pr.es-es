---
title: Problemas de autenticación para ADSI con ASP
description: En función de la configuración de la intranet, pueden producirse problemas de autenticación cuando se ejecuta código ADSI desde una página ASP.
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI, páginas ASP, problemas de autenticación
- ADSI, autenticación, problemas de ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793803"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>Problemas de autenticación para ADSI con ASP

En función de la configuración de la intranet, pueden producirse problemas de autenticación cuando se ejecuta código ADSI desde una página ASP.

La autenticación para tener acceso al controlador de dominio se puede conceder mediante la delegación. La delegación permite a un servicio actuar como usuario, por lo que puede tener acceso a un recurso de red mediante el uso de esas credenciales de usuario. Si la intranet sigue esta configuración, debe configurar IIS para utilizar la delegación. Establezca el mecanismo de autenticación de IIS como anónimo o NTLM. Si elige anónimo, el contexto de seguridad se asignará a la \_ cuenta de equipo IUSR. Si selecciona NTLM, el contexto de seguridad cambiará en función del usuario que inicie sesión en su sitio Web. Para obtener más información e instrucciones para configurar el servidor IIS para la delegación, vea [Kit de recursos de Windows 2000](https://support.microsoft.com/kb/927229).

Si usa un servidor IIS que usa el desafío/respuesta NT, o un cliente de explorador que no admite Kerberos, no se admite la autenticación de doble salto. La autenticación de doble salto significa que las credenciales del usuario se pasan desde el cliente del explorador al servidor IIS y, a continuación, el servidor IIS pasa las credenciales al servidor back-end. En esta situación, puede usar una de las siguientes soluciones para permitir el acceso al directorio desde la página ASP:

-   Use [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) para pasar credenciales a Active Directory. La página web autentica al usuario conectado con el servidor IIS. Cuando el usuario se ha autenticado, la página web puede usar OpenDSObject o ADsOpenObject para pasar un nombre de usuario y una contraseña al servicio de directorio para obtener la autenticación en el servidor back-end. La página web puede tener acceso a los datos desde el directorio.
-   Agregue el código a un objeto COM y colóquelo en una [aplicación com+](../cossdk/com--application-overview.md) (anteriormente denominada paquete mts). La aplicación COM+ puede ejecutarse como una [cuenta de usuario de dominio](/windows/desktop/AD/domain-user-accounts).
-   Usar varias páginas ASP, donde una página autentica al cliente y otra página pasa credenciales al directorio mediante la autenticación anónima en una cuenta de usuario de dominio.

Estos métodos implican la autenticación del cliente web y el cambio de las credenciales al ponerse en contacto con el directorio, ya que no es posible la autenticación de doble salto con las mismas credenciales.

 

 