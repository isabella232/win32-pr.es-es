---
description: Para llamar correctamente a la API de copia de seguridad y restauración de servicios de certificados, el token del llamador debe incluir los privilegios de copia de seguridad y restauración.
ms.assetid: 409a9fad-7141-4ba8-ab3d-fb590366001e
title: Establecer los privilegios de copia de seguridad y restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd70c3726c435efa1f000add101bbf50b725bb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666215"
---
# <a name="setting-the-backup-and-restore-privileges"></a><span data-ttu-id="8eb8d-103">Establecer los privilegios de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="8eb8d-103">Setting the Backup and Restore Privileges</span></span>

<span data-ttu-id="8eb8d-104">Para llamar correctamente a la API de copia de seguridad y restauración de servicios de certificados, el token del llamador debe incluir los [*privilegios*](../secgloss/p-gly.md)de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="8eb8d-104">To successfully call the Certificate Services backup and restore API, the caller's token must include the backup and restore [*privileges*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="8eb8d-105">Estos privilegios se pueden establecer mediante programación y el ejemplo siguiente se puede utilizar para establecer o quitar estos privilegios.</span><span class="sxs-lookup"><span data-stu-id="8eb8d-105">These privileges can be programmatically set, and the following example can be used to set or remove these privileges.</span></span> <span data-ttu-id="8eb8d-106">Los privilegios de copia de seguridad y restauración son necesarios para todas las aplicaciones de copia de seguridad y restauración, no solo para copias de seguridad y restauración de servicios de Certificate Server.</span><span class="sxs-lookup"><span data-stu-id="8eb8d-106">The backup and restore privileges are required of all backup and restore applications, not merely Certificate Services backup and restore.</span></span> <span data-ttu-id="8eb8d-107">Para obtener información sobre las implicaciones de seguridad de la modificación de privilegios, vea [ejecutar con privilegios especiales](../secbp/running-with-special-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="8eb8d-107">For information about the security implications of modifying privileges, see [Running with Special Privileges](../secbp/running-with-special-privileges.md).</span></span>


```C++
// The following example can be used to enable or disable the
// backup privilege. By making the indicated substitutions, you can
// also use this example to enable or disable the restore privilege 
// Use the following statement to enable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);
// Use the following statement to disable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, FALSE);
// Use SE_RESTORE_NAME for the restore privilege.
// The main function in this example enables the backup privilege.
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>


HRESULT ModifyPrivilege(
    IN LPCTSTR szPrivilege,
    IN BOOL fEnable)
{
    HRESULT hr = S_OK;
    TOKEN_PRIVILEGES NewState;
    LUID             luid;
    HANDLE hToken    = NULL;

    // Open the process token for this process.
    if (!OpenProcessToken(GetCurrentProcess(),
                          TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY,
                          &hToken ))
    {
        printf("Failed OpenProcessToken\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Get the local unique ID for the privilege.
    if ( !LookupPrivilegeValue( NULL,
                                szPrivilege,
                                &luid ))
    {
        CloseHandle( hToken );
        printf("Failed LookupPrivilegeValue\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Assign values to the TOKEN_PRIVILEGE structure.
    NewState.PrivilegeCount = 1;
    NewState.Privileges[0].Luid = luid;
    NewState.Privileges[0].Attributes = 
              (fEnable ? SE_PRIVILEGE_ENABLED : 0);

    // Adjust the token privilege.
    if (!AdjustTokenPrivileges(hToken,
                               FALSE,
                               &NewState,
                               0,
                               NULL,
                               NULL))
    {
        printf("Failed AdjustTokenPrivileges\n");
        hr = ERROR_FUNCTION_FAILED;
    }

    // Close the handle.
    CloseHandle(hToken);

    return hr;
}

void main(void)
{
    HRESULT hr;

    hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);

    if (!SUCCEEDED(hr))
        printf("\nFailed to modify privilege.\n");
    else
        printf("\nSuccessfully modified privilege.\n");
}

```



 

 
