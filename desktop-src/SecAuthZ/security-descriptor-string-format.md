---
description: El formato de cadena del descriptor de seguridad es un formato de texto para almacenar o transportar información en un descriptor de seguridad.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato de cadena del descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7fd6e9e2387deee63b5046086ed167a29fa54b
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644207"
---
# <a name="security-descriptor-string-format"></a>Formato de cadena del descriptor de seguridad

El **formato de cadena del descriptor de** seguridad es un formato de texto para almacenar o transportar información en un descriptor de seguridad. Las [**funciones ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usan este formato.

El formato es una cadena terminada en **NULL** con tokens para indicar cada uno de los cuatro componentes principales de un descriptor de seguridad: owner (O:), primary group (G:), DACL (D:) y SACL (S:).

> [!Note]  
> [*Las entradas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) y las ACE condicionales tienen formatos diferentes. Para las ACE, consulte [Ace Strings](ace-strings.md). Para las ACE condicionales, vea [Lenguaje de definición de descriptores de seguridad para ACE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>sid \_ de propietario
</dt> <dd>

Cadena [de SID](sid-strings.md) que identifica el propietario del objeto.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid
</dt> <dd>

Cadena de SID que identifica el grupo principal del objeto.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>marcas \_ dacl
</dt> <dd>

Marcas de control del descriptor de seguridad que se aplican a la DACL. Para obtener una descripción de estas marcas de control, vea la [**función SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) La cadena dacl \_ flags puede ser una concatenación de cero o más de las cadenas siguientes.



| Control               | Constante en Sddl.h       | Significado                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| "P"                   | SDDL \_ PROTECTED          | Se establece \_ la marca SE DACL \_ PROTECTED.          |
| "AR"                  | SDDL \_ AUTO \_ INHERIT \_ REQ | Se establece \_ la marca SE DACL AUTO INHERIT \_ \_ \_ REQ. |
| "IA"                  | SDDL \_ AUTO \_ INHERITED    | Se establece \_ la marca SE DACL AUTO \_ \_ INHERITED.    |
| "NO \_ ACCESS \_ CONTROL" | ACL NULL de SDDL \_ \_          | La ACL es null. **Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible. |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl \_ flags
</dt> <dd>

Marcas de control de descriptor de seguridad que se aplican a sacl. La cadena sacl \_ flags usa las mismas cadenas de bits de control que la cadena dacl \_ flags.

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace
</dt> <dd>

Cadena que describe una ACE en la DACL o SACL del descriptor de seguridad. Para obtener una descripción del formato de cadena ACE, vea [Ace strings](ace-strings.md). Cada cadena ACE se incluye entre paréntesis (()).

</dd> </dl>

Los componentes innecesarios se pueden omitir de la cadena del descriptor de seguridad. Por ejemplo, si la marca SE DACL PRESENT no está establecida en el descriptor de seguridad de \_ \_ entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) no incluye un componente D: en la cadena de salida. También puede usar las marcas de bits [**SECURITY \_ INFORMATION**](security-information.md) para indicar los componentes que se incluirán en una cadena de descriptor de seguridad.

El formato de cadena del descriptor de seguridad no admite **ACL NULL.**

Para indicar una ACL vacía, la cadena del descriptor de seguridad incluye el token D: o S: sin información de cadena adicional.

La cadena de descriptor de seguridad almacena los bits [**DE CONTROL DEL DESCRIPTOR DE SEGURIDAD**](security-descriptor-control.md) de maneras diferentes. Los bits SE DACL PRESENT o SE SACL PRESENT se indican mediante la presencia del \_ \_ token \_ \_ D: o S: en la cadena. Otros bits que se aplican a la DACL o SACL se almacenan en marcas dacl \_ y \_ sacl. Los bits SE \_ OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL DEFAULTED y SE \_ \_ SACL DEFAULTED no se almacenan \_ en una cadena de descriptor de seguridad. El bit SE SELF RELATIVE no se almacena en la cadena, pero \_ \_ [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) siempre establece este bit en el descriptor de seguridad de salida.

En los ejemplos siguientes se muestran cadenas de descriptores de seguridad y la información de los descriptores de seguridad asociados.

Cadena 1:


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Descriptor de seguridad 1:


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



Cadena 2:


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



Descriptor de seguridad 2:


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cadenas ACE](ace-strings.md)
</dt> <dt>

[Lenguaje de definición de descriptores de seguridad para A CA condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
