---
description: WMI tiene objetos y métodos que le permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a los objetos protegibles.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objetos de descriptor de seguridad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558749"
---
# <a name="wmi-security-descriptor-objects"></a>Objetos de descriptor de seguridad WMI

WMI tiene objetos y métodos que le permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a los objetos protegibles.

-   [El rol de los descriptores de seguridad](#the-role-of-security-descriptors)
-   [Objetos de seguridad de Access Control y WMI](#access-control-and-wmi-security-objects)
-   [\_Objeto SecurityDescriptor de Win32](/windows)
-   [DACL y SACL](#dacl-and-sacl)
-   [Win32 \_ ACE, \_ Administrador de confianza de Win32, SID de Win32 \_](/windows)
-   [Ejemplo: comprobar quién tiene acceso a las impresoras](#example-checking-who-has-access-to-printers)
-   [Temas relacionados](#related-topics)

## <a name="the-role-of-security-descriptors"></a>El rol de los descriptores de seguridad

Los descriptores de seguridad definen los atributos de seguridad de los objetos protegibles, como los archivos, las claves del registro, los espacios de nombres WMI, las impresoras, los servicios o los recursos compartidos. Un descriptor de seguridad contiene información sobre el propietario y el grupo primario de un objeto. Un proveedor puede comparar el descriptor de seguridad de recursos con la identidad de un usuario solicitante y determinar si el usuario tiene el derecho a acceder al recurso que solicita un usuario. Para obtener más información, vea [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).

Algunos métodos WMI, como se [**obtienen**](--systemsecurity-getsd.md), devuelven un descriptor de seguridad en el formato de matriz de bytes binaria. A partir de Windows Vista, use los métodos de la clase [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para convertir un descriptor de seguridad binario en una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), que se puede manipular más fácilmente. Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Objetos de seguridad de Access Control y WMI

A continuación se muestra una lista de objetos de seguridad WMI:

-   [**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**Administrador de confianza de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**SID de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

En el diagrama siguiente se muestran las relaciones existentes entre los objetos de seguridad WMI.

![relaciones entre objetos de seguridad WMI](images/security-descriptor.png)

Para obtener más información sobre el rol de seguridad de acceso, consulte [prácticas recomendadas de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis), mantenimiento de la [seguridad de WMI](maintaining-wmi-security.md)y [Access Control](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>\_Objeto SecurityDescriptor de Win32

En la tabla siguiente se enumeran las propiedades de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .



| Propiedad         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Conjunto de bits de control que califican el significado de un SD o sus miembros individuales. Para obtener más información acerca de cómo establecer los valores de bits **ControlFlags** , vea [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | [Lista de Access Control discrecional (ACL)](/windows/desktop/SecAuthZ/access-control-lists) de usuarios y grupos, así como sus derechos de acceso a un objeto protegido. Esta propiedad contiene una matriz de instancias de [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan [Access Control entradas](/windows/desktop/SecAuthZ/access-control-entries). Para obtener más información, vea [crear una DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Grupo**        | Grupo al que pertenece este objeto protegido. Esta propiedad contiene una instancia de [**\_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del grupo al que pertenece el propietario.<br/>                                                                                                                                                             |
| **Propietario**        | Propietario de este objeto protegido. Esta propiedad contiene una instancia de [ \_ Administrador de confianza de Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del propietario.<br/>                                                                                                                                                                                                          |
| **SACL**         | La [lista de Access Control del sistema (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contiene una matriz de instancias [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan el tipo de intentos de acceso que generan registros de auditoría para usuarios o grupos. Para obtener más información, vea [SACL para un nuevo objeto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL y SACL

Las matrices de objetos [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en la lista de control de acceso discrecional (DACL) y en la lista de control de acceso del sistema {SACL) crean un vínculo entre un usuario o un grupo y sus derechos de acceso.

Cuando una propiedad DACL no contiene una entrada de control de acceso (ACE), no se conceden derechos de acceso y se deniega el acceso al objeto.

> [!Note]  
> Una DACL **null** proporciona acceso completo a todos los usuarios, lo que supone un riesgo de seguridad grave. Para obtener más información, vea [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>Win32 \_ ACE, \_ Administrador de confianza de Win32, SID de Win32 \_

Un [**objeto \_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contiene una instancia de la clase de [**Administrador de \_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que identifica un usuario o grupo, y una propiedad **AccessMask** que es una máscara de máscara, que especifica las acciones que puede realizar un usuario o un grupo. Por ejemplo, se puede conceder a un usuario o grupo el derecho a leer un archivo pero no escribir en él. Un **objeto \_ ACE de Win32** también contiene una ACE que indica si es o no un acceso de permiso o denegación.

> [!Note]  
> El orden de [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en una DACL es importante porque las opciones permitir y denegar entrada de control de acceso (ACE) se permiten en una DACL. Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Cada cuenta de usuario o grupo representado por [**un \_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) tiene un identificador de seguridad (SID) que identifica de forma única una cuenta y especifica los privilegios de acceso de la cuenta. La forma de especificar los datos de SID depende del sistema operativo. Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

En el diagrama siguiente se muestra el contenido de una instancia de [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

![contenido de una instancia de ACE de Win32 \-](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Ejemplo: comprobar quién tiene acceso a las impresoras

En el ejemplo de código de VBScript siguiente se muestra cómo usar el descriptor de seguridad de la impresora. El script llama al método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) en la [**clase \_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) para obtener el descriptor y, a continuación, determina si hay una lista de Access Control discrecional (DACL) presente en el descriptor de seguridad. Si hay una DACL, el script obtiene la lista de entradas de Access Control (ACE) de la DACL. Cada ACE se representa mediante una instancia de [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). El script comprueba cada ACE para obtener el nombre del usuario y determinar si el usuario tiene acceso a la impresora. El usuario se representa en mediante una instancia de [**de \_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incrustada en la instancia de **\_ ACE de Win32** .


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

[Clase auxiliar de descriptor de seguridad](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Prácticas recomendadas de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Control de acceso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

