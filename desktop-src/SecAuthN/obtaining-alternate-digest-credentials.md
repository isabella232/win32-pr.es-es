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
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="247d5-103">Obtención de credenciales de Resumen alternativas</span><span class="sxs-lookup"><span data-stu-id="247d5-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="247d5-104">Para obtener [*credenciales*](../secgloss/c-gly.md) distintas de las asociadas a la [*sesión*](../secgloss/s-gly.md)de inicio de sesión actual, rellene una estructura de [**identidad de \_ \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC con información para la [*entidad de seguridad*](../secgloss/s-gly.md)alternativa.</span><span class="sxs-lookup"><span data-stu-id="247d5-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="247d5-105">Pase la estructura a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) mediante el parámetro *pAuthData* .</span><span class="sxs-lookup"><span data-stu-id="247d5-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="247d5-106">En la tabla siguiente se describen los miembros de la estructura de [**\_ identidad de \_ autenticación \_ de WinNT s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="247d5-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="247d5-107">Miembro</span><span class="sxs-lookup"><span data-stu-id="247d5-107">Member</span></span>             | <span data-ttu-id="247d5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="247d5-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247d5-109">**User**</span><span class="sxs-lookup"><span data-stu-id="247d5-109">**User**</span></span>           | <span data-ttu-id="247d5-110">Cadena terminada en null que contiene el nombre de la entidad de seguridad cuyas credenciales se usarán para establecer un contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="247d5-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="247d5-111">**UserLength**</span><span class="sxs-lookup"><span data-stu-id="247d5-111">**UserLength**</span></span>     | <span data-ttu-id="247d5-112">Longitud del miembro del **usuario** , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="247d5-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="247d5-113">Omita el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="247d5-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="247d5-114">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="247d5-114">**Domain**</span></span>         | <span data-ttu-id="247d5-115">Cadena terminada en null que identifica el dominio que contiene la cuenta de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="247d5-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="247d5-116">**DomainLength**</span><span class="sxs-lookup"><span data-stu-id="247d5-116">**DomainLength**</span></span>   | <span data-ttu-id="247d5-117">Longitud del miembro de **dominio** , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="247d5-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="247d5-118">Omita el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="247d5-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="247d5-119">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="247d5-119">**Password**</span></span>       | <span data-ttu-id="247d5-120">Cadena terminada en null que contiene la contraseña de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="247d5-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="247d5-121">**PasswordLength**</span><span class="sxs-lookup"><span data-stu-id="247d5-121">**PasswordLength**</span></span> | <span data-ttu-id="247d5-122">Longitud del miembro de **contraseña** , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="247d5-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="247d5-123">Omita el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="247d5-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="247d5-124">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="247d5-124">**Flags**</span></span>          | <span data-ttu-id="247d5-125">Indica si los miembros de cadena están en formato ANSI o [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="247d5-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="247d5-126">En la tabla siguiente se enumeran los valores válidos para el miembro **Flags** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="247d5-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="247d5-127">Constante</span><span class="sxs-lookup"><span data-stu-id="247d5-127">Constant</span></span>                            | <span data-ttu-id="247d5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="247d5-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247d5-129">SEG. de \_ \_ identidad de autenticación \_ \_ ANSI ANSI</span><span class="sxs-lookup"><span data-stu-id="247d5-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="247d5-130">Las cadenas de esta estructura están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="247d5-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="247d5-131">s de \_ autenticación WinNT de \_ \_ identidad \_ Unicode</span><span class="sxs-lookup"><span data-stu-id="247d5-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="247d5-132">Las cadenas de esta estructura están en formato [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="247d5-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="247d5-133">La estructura y las constantes se declaran en el archivo de encabezado Rpcdce. h distribuido con el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="247d5-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="247d5-134">En el ejemplo siguiente se muestra una llamada del lado cliente para obtener las credenciales de resumen para una cuenta de usuario específica.</span><span class="sxs-lookup"><span data-stu-id="247d5-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


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



<span data-ttu-id="247d5-135">La función **\_ tcslen** devuelve la longitud de la cadena en caracteres, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="247d5-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="247d5-136">Si su aplicación puede usar las credenciales establecidas en el inicio de sesión, consulte [obtención de credenciales de Resumen predeterminadas](obtaining-default-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="247d5-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
