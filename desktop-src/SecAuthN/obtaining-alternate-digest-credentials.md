---
description: Para obtener credenciales distintas de las asociadas a la sesión de inicio de sesión actual, rellene una \_ estructura de identidad de autenticación de WinNT de la SEC \_ \_ con información para la entidad de seguridad alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Obtención de credenciales de Resumen alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278123"
---
# <a name="obtaining-alternate-digest-credentials"></a>Obtención de credenciales de Resumen alternativas

Para obtener [*credenciales*](../secgloss/c-gly.md) distintas de las asociadas a la [*sesión*](../secgloss/s-gly.md)de inicio de sesión actual, rellene una estructura de [**identidad de \_ \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC con información para la [*entidad de seguridad*](../secgloss/s-gly.md)alternativa. Pase la estructura a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) mediante el parámetro *pAuthData* .

En la tabla siguiente se describen los miembros de la estructura de [**\_ identidad de \_ autenticación \_ de WinNT s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .



| Miembro             | Descripción                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **User**           | Cadena terminada en null que contiene el nombre de la entidad de seguridad cuyas credenciales se usarán para establecer un contexto de seguridad. |
| **UserLength**     | Longitud del miembro del **usuario** , en caracteres. Omita el carácter null de terminación.                                                         |
| **Dominio**         | Cadena terminada en null que identifica el dominio que contiene la cuenta de la entidad de seguridad.                                  |
| **DomainLength**   | Longitud del miembro de **dominio** , en caracteres. Omita el carácter null de terminación.                                                       |
| **Contraseña**       | Cadena terminada en null que contiene la contraseña de la entidad de seguridad.                                                            |
| **PasswordLength** | Longitud del miembro de **contraseña** , en caracteres. Omita el carácter null de terminación.                                                     |
| **Marcas**          | Indica si los miembros de cadena están en formato ANSI o [*Unicode*](../secgloss/u-gly.md) .  |



 

En la tabla siguiente se enumeran los valores válidos para el miembro **Flags** de la estructura.



| Constante                            | Descripción                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEG. de \_ \_ identidad de autenticación \_ \_ ANSI ANSI    | Las cadenas de esta estructura están en formato ANSI.                                                                    |
| s de \_ autenticación WinNT de \_ \_ identidad \_ Unicode | Las cadenas de esta estructura están en formato [*Unicode*](../secgloss/u-gly.md) . |



 

La estructura y las constantes se declaran en el archivo de encabezado Rpcdce. h distribuido con el kit de desarrollo de software (SDK) de la plataforma.

En el ejemplo siguiente se muestra una llamada del lado cliente para obtener las credenciales de resumen para una cuenta de usuario específica.


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



La función **\_ tcslen** devuelve la longitud de la cadena en caracteres, sin incluir el carácter nulo de terminación.

Si su aplicación puede usar las credenciales establecidas en el inicio de sesión, consulte [obtención de credenciales de Resumen predeterminadas](obtaining-default-digest-credentials.md).

 

 
