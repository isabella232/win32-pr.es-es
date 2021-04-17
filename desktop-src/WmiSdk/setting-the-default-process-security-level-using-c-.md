---
description: Cuando una aplicación cliente inicia sesión en Instrumental de administración de Windows (WMI) por primera vez, debe establecer el nivel de seguridad de proceso predeterminado con una llamada a CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Establecer el nivel de seguridad de proceso predeterminado mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546870"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Establecer el nivel de seguridad de proceso predeterminado mediante C++

Cuando una aplicación cliente inicia sesión en Instrumental de administración de Windows (WMI) por primera vez, debe establecer el nivel de seguridad de proceso predeterminado con una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM utiliza la información de la llamada para determinar cuánta seguridad debe tener otro proceso para tener acceso al proceso de la aplicación cliente.

En este tema se describen las siguientes secciones:

-   [Cambiar las credenciales de autenticación predeterminadas mediante C++](#changing-the-default-authentication-credentials-using-c)
-   [Cambiar los niveles de suplantación predeterminados mediante C++](#changing-the-default-impersonation-levels-using-c)

Para la mayoría de las aplicaciones cliente, los argumentos que se muestran en el ejemplo siguiente establecen la seguridad predeterminada para WMI.


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



El código requiere las siguientes referencias y \# instrucciones include para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Al establecer el nivel de autenticación en el nivel de autenticación de **RPC C, el \_ \_ \_ \_ valor predeterminado** permite que DCOM negocie el nivel de autenticación para que coincida con las demandas de seguridad del equipo de destino. Para obtener más información, vea [cambiar las credenciales de autenticación predeterminadas con c++](#changing-the-default-authentication-credentials-using-c) y [cambiar la configuración predeterminada de suplantación mediante c++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Cambiar las credenciales de autenticación predeterminadas mediante C++

Las credenciales de autenticación predeterminadas funcionan en la mayoría de las situaciones, pero es posible que tenga que usar credenciales de autenticación diferentes en situaciones diferentes. Por ejemplo, puede que desee agregar cifrado a los procedimientos de autenticación.

En la tabla siguiente se enumeran y describen los diferentes niveles de autenticación.



| Nivel de autenticación                 | Descripción                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ nivel predeterminado de autenticación de RPC C \_        | Autenticación de seguridad predeterminada.                                                      |
| nivel de autenticación de RPC \_ C \_ \_ \_ ninguno           | Sin autenticación.                                                                    |
| \_conexión de \_ nivel de \_ autenticación \_ de RPC C        | Autenticación solo cuando el cliente crea una relación con el servidor.           |
| \_llamada de \_ nivel de \_ autenticación \_ de RPC C           | Autenticación cada vez que el servidor recibe una RPC.                                  |
| \_PKT de \_ nivel de \_ autenticación \_ de RPC C            | Autenticación cada vez que el servidor recibe datos de un cliente.                      |
| integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_ | Autenticación que no se ha modificado ningún dato del paquete.                        |
| \_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_   | Incluye todos los niveles de autenticación anteriores y cifra el valor de cada llamada RPC. |



 

Puede especificar las credenciales de autenticación predeterminadas para varios usuarios mediante una única estructura de **\_ \_ lista de autenticación** en el parámetro *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

En el ejemplo de código siguiente se muestra cómo cambiar las credenciales de autenticación.


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a>Cambiar los niveles de suplantación predeterminados mediante C++

COM proporciona los niveles de seguridad predeterminados leídos del registro del sistema. Sin embargo, a menos que se modifiquen específicamente, la configuración del registro establece el nivel de suplantación demasiado bajo para que WMI funcione. Normalmente, el nivel de suplantación predeterminado es el **\_ \_ \_ nivel IMP \_ de RPC c**, pero WMI necesita al menos la **\_ \_ \_ \_ suplantación del nivel Imp de RPC c** para que funcione con la mayoría de los proveedores, y es posible que se produzca una situación en la que sea necesario establecer un nivel más alto de suplantación. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés). En la tabla siguiente se enumeran los diferentes niveles de suplantación.



| Nivel                           | Descripción                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ valor predeterminado de nivel de Imp \_ de RPC C     | El sistema operativo elige el nivel de suplantación.                                                      |
| \_nivel Imp de RPC C \_ \_ \_ anónimo   | El servidor puede suplantar al cliente, pero el token de suplantación no se puede usar para nada.               |
| \_identidad de \_ \_ nivel IMP \_ de RPC C    | El servidor puede obtener la identidad del cliente y suplantar al cliente para la comprobación de la ACL.                 |
| \_ \_ \_ Impersonate de nivel IMP \_ de RPC C | El servidor puede suplantar al cliente a través de un límite de equipo.                                           |
| \_delegado de \_ \_ nivel IMP \_ de RPC C    | El servidor puede suplantar al cliente en varios límites y puede realizar llamadas en nombre del cliente. |



 

 

 
