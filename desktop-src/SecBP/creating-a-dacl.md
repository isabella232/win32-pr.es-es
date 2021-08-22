---
description: Muestra cómo crear correctamente una DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Creación de una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516055"
---
# <a name="creating-a-dacl"></a>Creación de una DACL

La creación de una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) adecuada es una parte necesaria e importante del desarrollo de aplicaciones. Dado que **una** DACL NULL permite todos los tipos de acceso a todos los usuarios, no use DACL **NULL.**

En el ejemplo siguiente se muestra cómo crear correctamente una DACL. El ejemplo contiene una función, CreateMyDACL, que usa el lenguaje de definición de [descriptor](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de seguridad (SDDL) para definir el control de acceso concedido y denegado en una DACL. Para proporcionar acceso diferente a los objetos de la aplicación, modifique la función CreateMyDACL según sea necesario.

En el ejemplo:

1.  La función main pasa una dirección de una estructura [**ATRIBUTOS \_ DE SEGURIDAD**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) a la función CreateMyDACL.
2.  La función CreateMyDACL usa cadenas SDDL para:
    -   Denegar el acceso a usuarios de inicio de sesión anónimos y invitados.
    -   Permitir el acceso de lectura, escritura y ejecución a los usuarios autenticados.
    -   Permita el control total a los administradores.

    Para obtener más información sobre los formatos de cadena SDDL, vea [Formato de cadena del descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  La función CreateMyDACL llama a la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para convertir las cadenas SDDL en un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly). El miembro **lpSecurityDescriptor** de la estructura [**SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) señala al descriptor de seguridad. CreateMyDACL envía el valor devuelto de **ConvertStringSecurityDescriptorToSecurityDescriptor** a la función main.
4.  La función main usa la estructura [**SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) actualizada para especificar la DACL para una nueva carpeta creada por la [**función CreateDirectory.**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya)
5.  Cuando la función main termina de usar la estructura [**\_ ATRIBUTOS**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) DE SEGURIDAD, la función main libera la memoria asignada para el miembro **lpSecurityDescriptor** llamando a la [**función LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)

> [!Note]  
> Para compilar correctamente funciones SDDL como [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), debe definir la constante \_ WINNT win32 \_ como 0x0500 o superior.

 


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



 

 
