---
description: WMI tiene objetos y métodos que permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a objetos protegibles.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objetos de descriptor de seguridad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967003"
---
# <a name="wmi-security-descriptor-objects"></a>Objetos de descriptor de seguridad WMI

WMI tiene objetos y métodos que permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a objetos protegibles.

-   [El rol de los descriptores de seguridad](#the-role-of-security-descriptors)
-   [Access Control y objetos de seguridad WMI](#access-control-and-wmi-security-objects)
-   [Objeto \_ SecurityDescriptor de Win32](/windows)
-   [DACL y SACL](#dacl-and-sacl)
-   [Win32 \_ ACE, Win32 \_ Trustee, Win32 \_ SID](/windows)
-   [Ejemplo: Comprobación de Quién tiene acceso a impresoras](#example-checking-who-has-access-to-printers)
-   [Temas relacionados](#related-topics)

## <a name="the-role-of-security-descriptors"></a>El rol de los descriptores de seguridad

Los descriptores de seguridad definen los atributos de seguridad de objetos protegibles, como archivos, claves del Registro, espacios de nombres WMI, impresoras, servicios o recursos compartidos. Un descriptor de seguridad contiene información sobre el propietario y el grupo principal de un objeto . Un proveedor puede comparar el descriptor de seguridad de recursos con la identidad de un usuario solicitante y determinar si el usuario tiene o no derecho a acceder al recurso que solicita un usuario. Para obtener más información, vea [Acceso a objetos protegibles wmi.](access-to-wmi-securable-objects.md)

Algunos métodos WMI, como [**GetSD**](--systemsecurity-getsd.md), devuelven un descriptor de seguridad en el formato de matriz de bytes binario. A partir de Windows Vista, use los métodos de la clase [**\_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para convertir un descriptor de seguridad binario en una instancia de [**\_ SecurityDescriptor de Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)que se puede manipular más fácilmente. Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

## <a name="access-control-and-wmi-security-objects"></a>Access Control y objetos de seguridad WMI

A continuación se muestra una lista de objetos de seguridad WMI:

-   [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**Administrador de \_ Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**SID de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

En el diagrama siguiente se muestran las relaciones entre los objetos de seguridad WMI.

![relaciones entre objetos de seguridad wmi](images/security-descriptor.png)

Para obtener más información sobre el rol de seguridad de acceso, vea [Procedimientos](/windows/desktop/SecBP/best-practices-for-the-security-apis)recomendados de seguridad , Mantenimiento de la [seguridad WMI](maintaining-wmi-security.md)y [Access Control](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>Objeto \_ SecurityDescriptor de Win32

En la tabla siguiente se enumeran las propiedades de la clase [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)



| Propiedad         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Conjunto de bits de control que califican el significado de una SD o sus miembros individuales. Para obtener más información sobre cómo establecer los valores de bits **ControlFlags,** vea [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | [Lista de Access Control (ACL) de](/windows/desktop/SecAuthZ/access-control-lists) usuarios y grupos, así como sus derechos de acceso a un objeto protegido. Esta propiedad contiene una matriz de instancias ace de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan [Access Control entradas](/windows/desktop/SecAuthZ/access-control-entries). Para obtener más información, vea [Creación de una DACL.](/windows/desktop/SecBP/best-practices-for-the-security-apis)<br/> |
| **Grupo**        | Grupo al que pertenece este objeto protegido. Esta propiedad contiene una instancia de [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del grupo al que pertenece el propietario.<br/>                                                                                                                                                             |
| **Propietario**        | Propietario de este objeto protegido. Esta propiedad contiene una instancia de [Win32 \_ Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del propietario.<br/>                                                                                                                                                                                                          |
| **SACL**         | [System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contiene una matriz de instancias ace de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan el tipo de intentos de acceso que generan registros de auditoría para usuarios o grupos. Para obtener más información, [vea SACL para un nuevo objeto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL y SACL

Las matrices de objetos ACE de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en la lista de control de acceso discrecional (DACL) y la lista de control de acceso del sistema {SACL) crean un vínculo entre un usuario o grupo y sus derechos de acceso.

Cuando una propiedad DACL no contiene una entrada de control de acceso (ACE), no se conceden derechos de acceso y se deniega el acceso al objeto.

> [!Note]  
> Una **DACL NULL** proporciona acceso total a todos los usuarios, lo que supone un riesgo de seguridad grave. Para obtener más información, vea [Creación de una DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>Win32 \_ ACE, Win32 \_ Trustee, Win32 \_ SID

Un objeto ACE de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contiene una instancia de la clase De confianza de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que identifica un usuario o grupo, y una propiedad **AccessMask** que es una máscara de bits, que especifica las acciones que puede realizar un usuario o grupo. Por ejemplo, a un usuario o grupo se le podría conceder el derecho de leer un archivo, pero no escribir en él. Un **objeto \_ ACE de Win32** también contiene una ACE que indica si se trata de un acceso permitido o denegado.

> [!Note]  
> El [**orden \_ ace de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en una DACL es importante porque se permite la entrada de control de acceso (ACE) de permitir y denegar en una DACL. Para obtener más información, [vea Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Cada cuenta de usuario o grupo representado por un administrador de confianza de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) tiene un identificador de seguridad (SID) que identifica de forma única una cuenta y especifica los privilegios de acceso de la cuenta. La forma en que se especifican los datos de SID depende del sistema operativo. Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

En el diagrama siguiente se muestra el contenido de una [**instancia ace \_ de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)

![contenido de una instancia de win32 \- ace](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Ejemplo: Comprobación de Quién tiene acceso a impresoras

En el siguiente ejemplo de código de VBScript se muestra cómo usar el descriptor de seguridad de la impresora. El script llama al [**método GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la clase Printer de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-printer) para obtener el descriptor y, a continuación, determina si hay una lista de Access Control discrecional (DACL) presente en el descriptor de seguridad. Si hay una DACL, el script obtiene la lista de Access Control entradas (ACE) de la DACL. Cada ACE se representa mediante una instancia de [**ACE de \_ Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) El script comprueba cada ACE para obtener el nombre del usuario y determinar si el usuario tiene acceso a la impresora. El usuario se representa en mediante una instancia de [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) insertada en la **instancia ace de \_ Win32.**


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> <dt>

[Clase auxiliar del descriptor de seguridad](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Procedimientos recomendados de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Control de acceso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

