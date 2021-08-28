---
title: Cambiar la contraseña en la cuenta de usuario de un servicio
description: Para una instancia de servicio que inicia sesión con una cuenta de usuario, en lugar de con la cuenta LocalSystem, el Administrador de control de servicios (SCM) del equipo host almacena la contraseña de la cuenta, que usa para iniciar sesión en el servicio cuando se inicia el servicio.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Cambio de la contraseña en la cuenta de usuario de un servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66f0d7b4dc668697b7a0a8d5b120735f3a445cf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881626"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Cambiar la contraseña en la cuenta de usuario de un servicio

Para una instancia de servicio que inicia sesión con una cuenta de usuario, en lugar de con la cuenta LocalSystem, el Administrador de control de servicios (SCM) del equipo host almacena la contraseña de la cuenta, que usa para iniciar sesión en el servicio cuando se inicia el servicio. Al igual que con cualquier cuenta de usuario, debe cambiar la contraseña periódicamente para mantener la seguridad. Al cambiar la contraseña en una cuenta de servicio, actualice la contraseña almacenada por el SCM. En el ejemplo de código siguiente se muestra cómo realizar ambas acciones.

En los ejemplos de código [**se usa IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) para establecer la contraseña de la cuenta. Este método usa el nombre distintivo de la cuenta. A continuación, el ejemplo abre un identificador para el servicio instalado en el equipo host especificado y usa la función [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para actualizar la contraseña almacenada en caché por el SCM. Esta función usa el nombre SAM (" &lt; nombre de usuario de dominio ") de la &gt; \\ &lt; &gt; cuenta.

> [!Note]  
> Un administrador de dominio debe ejecutar este código.

 

Para un servicio replicable en el que cada réplica usa una cuenta de inicio de sesión diferente, puede actualizar las contraseñas de todas las réplicas enumerando las instancias de servicio. Para obtener más información y un ejemplo de código, [vea Enumerar las réplicas de un servicio](enumerating-the-replicas-of-a-service.md).


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



 

 
