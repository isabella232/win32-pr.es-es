---
description: Muestra cómo crear correctamente una DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Crear una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912837"
---
# <a name="creating-a-dacl"></a>Crear una DACL

Crear una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) adecuada es una parte necesaria y importante del desarrollo de aplicaciones. Dado que una DACL **null** permite todos los tipos de acceso a todos los usuarios, no use listas DACL **nulas** .

En el ejemplo siguiente se muestra cómo crear correctamente una DACL. El ejemplo contiene una función, CreateMyDACL, que usa el [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) para definir el control de acceso concedido y denegado en una DACL. Para proporcionar un acceso diferente para los objetos de la aplicación, modifique la función CreateMyDACL según sea necesario.

En el ejemplo:

1.  La función Main pasa una dirección de una estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) a la función CreateMyDACL.
2.  La función CreateMyDACL usa cadenas SDDL para:
    -   Denegar el acceso a usuarios de inicio de sesión anónimo y invitado.
    -   Permitir el acceso de lectura/escritura/ejecución a los usuarios autenticados.
    -   Permitir el control total para los administradores.

    Para obtener más información sobre los formatos de cadena SDDL, vea el [formato de cadena de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  La función CreateMyDACL llama a la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para convertir las cadenas SDDL en un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly). El miembro **lpSecurityDescriptor** de la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) apunta al descriptor de seguridad. CreateMyDACL envía el valor devuelto de **ConvertStringSecurityDescriptorToSecurityDescriptor** a la función main.
4.  La función Main utiliza la estructura [**de \_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) actualizada para especificar la DACL para una nueva carpeta que se crea mediante la función [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .
5.  Cuando la función Main termina de usar la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , la función Main libera la memoria asignada para el miembro **lpSecurityDescriptor** llamando a la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

> [!Note]  
> Para compilar correctamente funciones de SDDL como [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), debe definir \_ la \_ constante WinNT de Win32 como 0x0500 o superior.

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
