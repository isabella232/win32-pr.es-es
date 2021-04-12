---
title: Cambio de la contraseña en la cuenta de usuario de un servicio
description: En el caso de una instancia de servicio que inicia sesión con una cuenta de usuario, en lugar de la cuenta LocalSystem, el administrador de control de servicios (SCM) del equipo host almacena la contraseña de la cuenta, que usa para iniciar sesión en el servicio cuando se inicia el servicio.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Cambio de la contraseña en la cuenta de usuario del servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf16b018796979d3710825472a5f9abab72cd24
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487499"
---
# <a name="changing-the-password-on-a-services-user-account"></a><span data-ttu-id="b0cea-104">Cambio de la contraseña en la cuenta de usuario de un servicio</span><span class="sxs-lookup"><span data-stu-id="b0cea-104">Changing the Password on a Service's User Account</span></span>

<span data-ttu-id="b0cea-105">En el caso de una instancia de servicio que inicia sesión con una cuenta de usuario, en lugar de la cuenta LocalSystem, el administrador de control de servicios (SCM) del equipo host almacena la contraseña de la cuenta, que usa para iniciar sesión en el servicio cuando se inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="b0cea-105">For a service instance that logs on with a user account, rather than the LocalSystem account, the Service Control Manager (SCM) on the host computer stores the account password, which it uses to log on the service when the service starts.</span></span> <span data-ttu-id="b0cea-106">Como con cualquier cuenta de usuario, debe cambiar la contraseña periódicamente para mantener la seguridad.</span><span class="sxs-lookup"><span data-stu-id="b0cea-106">As with any user account, you must change the password periodically to maintain security.</span></span> <span data-ttu-id="b0cea-107">Cuando cambie la contraseña en una cuenta de servicio, actualice la contraseña almacenada por el SCM.</span><span class="sxs-lookup"><span data-stu-id="b0cea-107">When you change the password on a service account, update the password stored by the SCM.</span></span> <span data-ttu-id="b0cea-108">En el ejemplo de código siguiente se muestra cómo realizar ambas operaciones.</span><span class="sxs-lookup"><span data-stu-id="b0cea-108">The following code example shows how to do both.</span></span>

<span data-ttu-id="b0cea-109">En los ejemplos de código se usa [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) para establecer la contraseña de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b0cea-109">The code examples use [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) to set the account password.</span></span> <span data-ttu-id="b0cea-110">Este método usa el nombre distintivo de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b0cea-110">This method uses the distinguished name of the account.</span></span> <span data-ttu-id="b0cea-111">A continuación, el ejemplo abre un identificador para el servicio instalado en el equipo host especificado y usa la función [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para actualizar la contraseña almacenada en caché por el SCM.</span><span class="sxs-lookup"><span data-stu-id="b0cea-111">Then the sample opens a handle to the installed service on the specified host computer, and uses the [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) function to update the password cached by the SCM.</span></span> <span data-ttu-id="b0cea-112">Esta función usa el nombre Sam (" <domain> \\ <username> ") de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b0cea-112">This function uses the SAM name ("<domain>\\<username>") of the account.</span></span>

> [!Note]  
> <span data-ttu-id="b0cea-113">Este código debe ser ejecutado por un administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b0cea-113">This code must be executed by a domain administrator.</span></span>

 

<span data-ttu-id="b0cea-114">En el caso de un servicio replicable en el que cada réplica use una cuenta de inicio de sesión diferente, puede actualizar las contraseñas de todas las réplicas mediante la enumeración de las instancias de servicio.</span><span class="sxs-lookup"><span data-stu-id="b0cea-114">For a replicable service in which each replica uses a different logon account, you could update the passwords for all of the replicas by enumerating the service instances.</span></span> <span data-ttu-id="b0cea-115">Para obtener más información y un ejemplo de código, consulte [enumeración de las réplicas de un servicio](enumerating-the-replicas-of-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="b0cea-115">For more information and a code example, see [Enumerating the Replicas of a Service](enumerating-the-replicas-of-a-service.md).</span></span>


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 