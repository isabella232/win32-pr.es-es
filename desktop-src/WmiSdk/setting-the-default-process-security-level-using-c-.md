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
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="f4a6d-103">Establecer el nivel de seguridad de proceso predeterminado mediante C++</span><span class="sxs-lookup"><span data-stu-id="f4a6d-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="f4a6d-104">Cuando una aplicación cliente inicia sesión en Instrumental de administración de Windows (WMI) por primera vez, debe establecer el nivel de seguridad de proceso predeterminado con una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f4a6d-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f4a6d-105">COM utiliza la información de la llamada para determinar cuánta seguridad debe tener otro proceso para tener acceso al proceso de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="f4a6d-106">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f4a6d-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="f4a6d-107">Cambiar las credenciales de autenticación predeterminadas mediante C++</span><span class="sxs-lookup"><span data-stu-id="f4a6d-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="f4a6d-108">Cambiar los niveles de suplantación predeterminados mediante C++</span><span class="sxs-lookup"><span data-stu-id="f4a6d-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="f4a6d-109">Para la mayoría de las aplicaciones cliente, los argumentos que se muestran en el ejemplo siguiente establecen la seguridad predeterminada para WMI.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


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



<span data-ttu-id="f4a6d-110">El código requiere las siguientes referencias y \# instrucciones include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="f4a6d-111">Al establecer el nivel de autenticación en el nivel de autenticación de **RPC C, el \_ \_ \_ \_ valor predeterminado** permite que DCOM negocie el nivel de autenticación para que coincida con las demandas de seguridad del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="f4a6d-112">Para obtener más información, vea [cambiar las credenciales de autenticación predeterminadas con c++](#changing-the-default-authentication-credentials-using-c) y [cambiar la configuración predeterminada de suplantación mediante c++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="f4a6d-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="f4a6d-113">Cambiar las credenciales de autenticación predeterminadas mediante C++</span><span class="sxs-lookup"><span data-stu-id="f4a6d-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="f4a6d-114">Las credenciales de autenticación predeterminadas funcionan en la mayoría de las situaciones, pero es posible que tenga que usar credenciales de autenticación diferentes en situaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="f4a6d-115">Por ejemplo, puede que desee agregar cifrado a los procedimientos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="f4a6d-116">En la tabla siguiente se enumeran y describen los diferentes niveles de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="f4a6d-117">Nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="f4a6d-117">Authentication level</span></span>                 | <span data-ttu-id="f4a6d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4a6d-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a6d-119">\_ \_ \_ nivel predeterminado de autenticación de RPC C \_</span><span class="sxs-lookup"><span data-stu-id="f4a6d-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="f4a6d-120">Autenticación de seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="f4a6d-121">nivel de autenticación de RPC \_ C \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f4a6d-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="f4a6d-122">Sin autenticación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="f4a6d-123">\_conexión de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="f4a6d-124">Autenticación solo cuando el cliente crea una relación con el servidor.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="f4a6d-125">\_llamada de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="f4a6d-126">Autenticación cada vez que el servidor recibe una RPC.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="f4a6d-127">\_PKT de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="f4a6d-128">Autenticación cada vez que el servidor recibe datos de un cliente.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="f4a6d-129">integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4a6d-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="f4a6d-130">Autenticación que no se ha modificado ningún dato del paquete.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="f4a6d-131">\_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_</span><span class="sxs-lookup"><span data-stu-id="f4a6d-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="f4a6d-132">Incluye todos los niveles de autenticación anteriores y cifra el valor de cada llamada RPC.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="f4a6d-133">Puede especificar las credenciales de autenticación predeterminadas para varios usuarios mediante una única estructura de **\_ \_ lista de autenticación** en el parámetro *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f4a6d-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="f4a6d-134">En el ejemplo de código siguiente se muestra cómo cambiar las credenciales de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-134">The following code example shows how to change the authentication credentials.</span></span>


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



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="f4a6d-135">Cambiar los niveles de suplantación predeterminados mediante C++</span><span class="sxs-lookup"><span data-stu-id="f4a6d-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="f4a6d-136">COM proporciona los niveles de seguridad predeterminados leídos del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="f4a6d-137">Sin embargo, a menos que se modifiquen específicamente, la configuración del registro establece el nivel de suplantación demasiado bajo para que WMI funcione.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="f4a6d-138">Normalmente, el nivel de suplantación predeterminado es el **\_ \_ \_ nivel IMP \_ de RPC c**, pero WMI necesita al menos la **\_ \_ \_ \_ suplantación del nivel Imp de RPC c** para que funcione con la mayoría de los proveedores, y es posible que se produzca una situación en la que sea necesario establecer un nivel más alto de suplantación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="f4a6d-139">Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).</span><span class="sxs-lookup"><span data-stu-id="f4a6d-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="f4a6d-140">En la tabla siguiente se enumeran los diferentes niveles de suplantación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="f4a6d-141">Nivel</span><span class="sxs-lookup"><span data-stu-id="f4a6d-141">Level</span></span>                           | <span data-ttu-id="f4a6d-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4a6d-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a6d-143">\_ \_ \_ valor predeterminado de nivel de Imp \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="f4a6d-144">El sistema operativo elige el nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="f4a6d-145">\_nivel Imp de RPC C \_ \_ \_ anónimo</span><span class="sxs-lookup"><span data-stu-id="f4a6d-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="f4a6d-146">El servidor puede suplantar al cliente, pero el token de suplantación no se puede usar para nada.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="f4a6d-147">\_identidad de \_ \_ nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="f4a6d-148">El servidor puede obtener la identidad del cliente y suplantar al cliente para la comprobación de la ACL.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="f4a6d-149">\_ \_ \_ Impersonate de nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="f4a6d-150">El servidor puede suplantar al cliente a través de un límite de equipo.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="f4a6d-151">\_delegado de \_ \_ nivel IMP \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="f4a6d-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="f4a6d-152">El servidor puede suplantar al cliente en varios límites y puede realizar llamadas en nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
