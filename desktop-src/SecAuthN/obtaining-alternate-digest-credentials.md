---
description: Para obtener credenciales que no son las asociadas a la sesión de inicio de sesión actual, rellene una estructura SEC WINNT AUTH IDENTITY con información para la \_ \_ entidad de seguridad \_ alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Obtención de credenciales implícitas alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260aa1c4cb3bd52395352e2e5dcadcaed7e3fea3cf478367a9e3432c7d2c8d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921294"
---
# <a name="obtaining-alternate-digest-credentials"></a>Obtención de credenciales implícitas alternativas

Para obtener [*credenciales*](../secgloss/c-gly.md) que no son las asociadas a la sesión de inicio de sesión [*actual,*](../secgloss/s-gly.md)rellene una estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) con información para la entidad de [*seguridad alternativa*](../secgloss/s-gly.md). Pase la estructura a la [**función AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) mediante el *parámetro pAuthData.*

En la tabla siguiente se describen los miembros de la estructura [**\_ SEC WINNT \_ AUTH \_ IDENTITY.**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)



| Miembro             | Descripción                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **User**           | Cadena terminada en NULL que contiene el nombre de la entidad de seguridad cuyas credenciales se usarán para establecer un contexto de seguridad. |
| **UserLength**     | Longitud del miembro **User,** en caracteres. Omita el valor null de terminación.                                                         |
| **Dominio**         | Cadena terminada en NULL que identifica el dominio que contiene la cuenta de la entidad de seguridad.                                  |
| **DomainLength**   | Longitud del miembro **Domain,** en caracteres. Omita el valor null de terminación.                                                       |
| **Contraseña**       | Cadena terminada en NULL que contiene la contraseña de la entidad de seguridad.                                                            |
| **PasswordLength** | Longitud del miembro **Password,** en caracteres. Omita el valor null de terminación.                                                     |
| **Marcas**          | Indica si los miembros de cadena están en formato ANSI [*o Unicode.*](../secgloss/u-gly.md)  |



 

En la tabla siguiente se enumeran los valores válidos para el **miembro Flags** de la estructura .



| Constante                            | Descripción                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| ANSI DE \_ IDENTIDAD DE AUTENTICACIÓN DE WINNT \_ \_ \_ SEC    | Las cadenas de esta estructura están en formato ANSI.                                                                    |
| UNICODE \_ DE IDENTIDAD DE AUTENTICACIÓN DE WINNT \_ \_ DE \_ SEGUNDO | Las cadenas de esta estructura están en [*formato Unicode.*](../secgloss/u-gly.md) |



 

La estructura y las constantes se declaran en el archivo de encabezado Rpcdce.h distribuido con el Kit de desarrollo de software (SDK) de plataforma.

En el ejemplo siguiente se muestra una llamada del lado cliente para obtener las credenciales implícitas de una cuenta de usuario específica.


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



La **\_ función tcslen** devuelve la longitud de cadena en caracteres, sin incluir el carácter nulo de terminación.

Si la aplicación puede usar las credenciales establecidas en el inicio de sesión, consulte [Obtención de credenciales implícitas predeterminadas.](obtaining-default-digest-credentials.md)

 

 
