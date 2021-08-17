---
description: La habilitación de un privilegio en un token de acceso permite al proceso realizar acciones de nivel de sistema que no se podían realizar anteriormente.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Habilitación y deshabilitación de privilegios en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781731"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Habilitación y deshabilitación de privilegios en C++

La habilitación de un privilegio en un token de acceso permite al proceso realizar acciones de nivel de sistema que no se podían realizar anteriormente. La aplicación debe comprobar exhaustivamente que el privilegio es adecuado para el tipo de cuenta, especialmente para los siguientes privilegios eficaces.



| Constante de privilegios           | Valor de cadena                  | Nombre para mostrar                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_SE ASSIGNPRIMARYTOKEN \_ NAME | SeAssignPrimaryTokenPrivilege | Reemplazar un token de nivel de proceso       |
| \_SE NOMBRE DE COPIA \_ DE SEGURIDAD             | SeBackupPrivilege             | Hacer copias de seguridad de archivos y directorios       |
| \_SE NOMBRE DE \_ DEPURACIÓN              | SeDebugPrivilege              | Programas de depuración                      |
| \_SE AUMENTAR EL \_ NOMBRE DE \_ CUOTA    | SeIncreaseQuotaPrivilege      | Ajustar las cuotas de la memoria para un proceso  |
| \_SE NOMBRE \_ DE TCB                | SeTcbPrivilege                | Actuar como parte del sistema operativo |



 

Antes de habilitar cualquiera de estos privilegios potencialmente peligrosos, determine que las funciones u operaciones del código realmente requieren los privilegios. Por ejemplo, muy pocas funciones del sistema operativo requieren realmente **SeTcbPrivilege**. Para obtener una lista de todos los privilegios disponibles, vea [Constantes de privilegios](authorization-constants.md).

En el ejemplo siguiente se muestra cómo habilitar o deshabilitar un privilegio en un [*token de acceso*](/windows/desktop/SecGloss/a-gly). En el ejemplo se [**llama a la función LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obtener el identificador único [*local*](/windows/desktop/SecGloss/l-gly) (LUID) que el sistema local usa para identificar el privilegio. A continuación, el ejemplo llama a la función [**AdjustTokenPrivileges,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) que habilita o deshabilita el privilegio que depende del valor del *parámetro bEnablePrivilege.*


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



 

