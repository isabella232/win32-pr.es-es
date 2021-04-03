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
# <a name="enabling-and-disabling-privileges-in-c"></a>Habilitar y deshabilitar privilegios en C++

La habilitación de un privilegio en un token de acceso permite que el proceso realice acciones de nivel de sistema que no pudo realizar previamente. La aplicación debe comprobar exhaustivamente que el privilegio es adecuado para el tipo de cuenta, especialmente para los siguientes privilegios eficaces.



| Constante de privilegios           | Valor de cadena                  | Nombre para mostrar                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_nombre de ASSIGNPRIMARYTOKEN se \_ | SeAssignPrimaryTokenPrivilege | Reemplazar un token de nivel de proceso       |
| nombre de copia de seguridad de SE \_ \_             | SeBackupPrivilege             | Hacer copias de seguridad de archivos y directorios       |
| \_nombre de depuración de se \_              | SeDebugPrivilege              | Programas de depuración                      |
| SE \_ ha \_ aumentado \_ el nombre de la cuota    | SeIncreaseQuotaPrivilege      | Ajustar las cuotas de la memoria para un proceso  |
| nombre de la \_ TCB \_                | SeTcbPrivilege                | Actuar como parte del sistema operativo |



 

Antes de habilitar cualquiera de estos privilegios potencialmente peligrosos, determine que las funciones u operaciones del código requieren realmente los privilegios. Por ejemplo, muy pocas funciones del sistema operativo realmente requieren el **SeTcbPrivilege**. Para obtener una lista de todos los privilegios disponibles, consulte [constantes de privilegios](authorization-constants.md).

En el ejemplo siguiente se muestra cómo habilitar o deshabilitar un privilegio en un [*token de acceso*](/windows/desktop/SecGloss/a-gly). En el ejemplo se llama a la función [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obtener el [*identificador local único*](/windows/desktop/SecGloss/l-gly) (LUID) que el sistema local usa para identificar el privilegio. A continuación, en el ejemplo se llama a la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , que habilita o deshabilita el privilegio que depende del valor del parámetro *bEnablePrivilege* .


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



 

