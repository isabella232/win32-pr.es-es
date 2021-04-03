---
description: La habilitación de un privilegio en un token de acceso permite que el proceso realice acciones de nivel de sistema que no pudo realizar previamente.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Habilitar y deshabilitar privilegios en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083149"
---
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="c6f2d-103">Habilitar y deshabilitar privilegios en C++</span><span class="sxs-lookup"><span data-stu-id="c6f2d-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="c6f2d-104">La habilitación de un privilegio en un token de acceso permite que el proceso realice acciones de nivel de sistema que no pudo realizar previamente.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="c6f2d-105">La aplicación debe comprobar exhaustivamente que el privilegio es adecuado para el tipo de cuenta, especialmente para los siguientes privilegios eficaces.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="c6f2d-106">Constante de privilegios</span><span class="sxs-lookup"><span data-stu-id="c6f2d-106">Privilege constant</span></span>           | <span data-ttu-id="c6f2d-107">Valor de cadena</span><span class="sxs-lookup"><span data-stu-id="c6f2d-107">String value</span></span>                  | <span data-ttu-id="c6f2d-108">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="c6f2d-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="c6f2d-109">\_nombre de ASSIGNPRIMARYTOKEN se \_</span><span class="sxs-lookup"><span data-stu-id="c6f2d-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="c6f2d-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="c6f2d-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="c6f2d-111">Reemplazar un token de nivel de proceso</span><span class="sxs-lookup"><span data-stu-id="c6f2d-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="c6f2d-112">nombre de copia de seguridad de SE \_ \_</span><span class="sxs-lookup"><span data-stu-id="c6f2d-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="c6f2d-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="c6f2d-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="c6f2d-114">Hacer copias de seguridad de archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="c6f2d-114">Back up files and directories</span></span>       |
| <span data-ttu-id="c6f2d-115">\_nombre de depuración de se \_</span><span class="sxs-lookup"><span data-stu-id="c6f2d-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="c6f2d-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="c6f2d-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="c6f2d-117">Programas de depuración</span><span class="sxs-lookup"><span data-stu-id="c6f2d-117">Debug programs</span></span>                      |
| <span data-ttu-id="c6f2d-118">SE \_ ha \_ aumentado \_ el nombre de la cuota</span><span class="sxs-lookup"><span data-stu-id="c6f2d-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="c6f2d-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="c6f2d-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="c6f2d-120">Ajustar las cuotas de la memoria para un proceso</span><span class="sxs-lookup"><span data-stu-id="c6f2d-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="c6f2d-121">nombre de la \_ TCB \_</span><span class="sxs-lookup"><span data-stu-id="c6f2d-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="c6f2d-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="c6f2d-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="c6f2d-123">Actuar como parte del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6f2d-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="c6f2d-124">Antes de habilitar cualquiera de estos privilegios potencialmente peligrosos, determine que las funciones u operaciones del código requieren realmente los privilegios.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="c6f2d-125">Por ejemplo, muy pocas funciones del sistema operativo realmente requieren el **SeTcbPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="c6f2d-126">Para obtener una lista de todos los privilegios disponibles, consulte [constantes de privilegios](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c6f2d-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="c6f2d-127">En el ejemplo siguiente se muestra cómo habilitar o deshabilitar un privilegio en un [*token de acceso*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="c6f2d-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="c6f2d-128">En el ejemplo se llama a la función [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obtener el [*identificador local único*](/windows/desktop/SecGloss/l-gly) (LUID) que el sistema local usa para identificar el privilegio.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="c6f2d-129">A continuación, en el ejemplo se llama a la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , que habilita o deshabilita el privilegio que depende del valor del parámetro *bEnablePrivilege* .</span><span class="sxs-lookup"><span data-stu-id="c6f2d-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

