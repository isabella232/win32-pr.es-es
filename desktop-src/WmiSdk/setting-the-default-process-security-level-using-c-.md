---
description: Cuando una aplicación cliente inicia sesión en Windows Management Instrumentation (WMI) por primera vez, debe establecer el nivel de seguridad del proceso predeterminado con una llamada a CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Establecer el nivel de seguridad de proceso predeterminado mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050293"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Establecer el nivel de seguridad de proceso predeterminado mediante C++

Cuando una aplicación cliente inicia sesión en Windows Management Instrumentation (WMI) por primera vez, debe establecer el nivel de seguridad del proceso predeterminado con una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM usa la información de la llamada para determinar la seguridad que debe tener otro proceso para acceder al proceso de aplicación cliente.

En este tema se de abordan las siguientes secciones:

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



El código requiere las siguientes referencias e \# instrucciones include para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Establecer el nivel de autenticación en **RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT** permite a DCOM negociar el nivel de autenticación para que coincida con las demandas de seguridad del equipo de destino. Para obtener más información, vea Cambiar las credenciales de [autenticación predeterminadas](#changing-the-default-authentication-credentials-using-c) mediante C++ y Cambiar la suplantación [predeterminada Configuración usar C++.](#changing-the-default-impersonation-levels-using-c)

## <a name="changing-the-default-authentication-credentials-using-c"></a>Cambiar las credenciales de autenticación predeterminadas mediante C++

Las credenciales de autenticación predeterminadas funcionan en la mayoría de las situaciones, pero es posible que tenga que usar credenciales de autenticación diferentes en situaciones diferentes. Por ejemplo, es posible que desee agregar cifrado a los procedimientos de autenticación.

En la tabla siguiente se enumeran y describen los distintos niveles de autenticación.



| Nivel de autenticación                 | Descripción                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT        | Autenticación de seguridad predeterminada.                                                      |
| RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           | Sin autenticación.                                                                    |
| CONEXIÓN \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE RPC C \_        | Autenticación solo cuando el cliente crea una relación con el servidor.           |
| LLAMADA \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE RPC C \_           | Autenticación cada vez que el servidor recibe una RPC.                                  |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            | Autenticación cada vez que el servidor recibe datos de un cliente.                      |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY | Autenticación en la que no se ha modificado ningún dato del paquete.                        |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   | Incluye todos los niveles de autenticación anteriores y cifra el valor de cada llamada RPC. |



 

Puede especificar las credenciales de autenticación predeterminadas para varios usuarios mediante una estructura **\_ SOLE AUTHENTICATION \_ LIST** en el *parámetro pAuthList* [**de CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

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

COM proporciona niveles de seguridad predeterminados leídos del registro del sistema. Sin embargo, a menos que se modifique específicamente, la configuración del Registro establece el nivel de suplantación demasiado bajo para que WMI funcione. Normalmente, el nivel de suplantación predeterminado es **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY**, pero WMI necesita al menos **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE** para funcionar con la mayoría de los proveedores y puede encontrarse con una situación en la que necesite establecer un nivel superior de suplantación. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés). En la tabla siguiente se enumeran los distintos niveles de suplantación.



| Nivel                           | Descripción                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT     | El sistema operativo elige el nivel de suplantación.                                                      |
| RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   | El servidor puede suplantar al cliente, pero el token de suplantación no se puede usar para nada.               |
| RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    | El servidor puede obtener la identidad del cliente y suplantar al cliente para la comprobación de ACL.                 |
| \_SUPLANTACIÓN DE NIVEL DE IMP \_ \_ \_ DE RPC C | El servidor puede suplantar al cliente a través de un límite de equipo.                                           |
| RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE    | El servidor puede suplantar al cliente a través de varios límites y puede realizar llamadas en nombre del cliente. |



 

 

 
