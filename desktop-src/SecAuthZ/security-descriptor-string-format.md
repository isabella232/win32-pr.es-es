---
description: El formato de cadena de descriptor de seguridad es un formato de texto para almacenar o transportar información en un descriptor de seguridad.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Formato de cadena de descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908170"
---
# <a name="security-descriptor-string-format"></a>Formato de cadena de descriptor de seguridad

El **formato de cadena de descriptor de seguridad** es un formato de texto para almacenar o transportar información en un descriptor de seguridad. Las funciones [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usan este formato.

El formato es una cadena terminada en **null** con tokens para indicar cada uno de los cuatro componentes principales de un descriptor de seguridad: Owner (o:), Primary Group (G:), DACL (D:) y SACL (s:).

> [!Note]  
> [*Las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) y las ACE condicionales tienen distintos formatos. Para las ACE, consulte [cadenas ACE](ace-strings.md). Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>SID de propietario \_
</dt> <dd>

[Cadena SID](sid-strings.md) que identifica el propietario del objeto.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>SID de grupo \_
</dt> <dd>

Cadena SID que identifica el grupo primario del objeto.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>marcas de DACL \_
</dt> <dd>

Marcas de control de descriptor de seguridad que se aplican a la DACL. Para obtener una descripción de estas marcas de control, consulte la función [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . La \_ cadena de marcas de DACL puede ser una concatenación de cero o más de las siguientes cadenas.



| Control               | Constante en SDDL. h       | Significado                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| M                   | SDDL \_ protegido          | \_Se establece la marca protegida de DACL de se \_ .          |
| ANALÍTICO                  | \_solicitud de \_ herencia \_ automática de SDDL | \_ \_ \_ Se establece la marca req de herencia automática de DACL de se \_ . |
| EMPLEADOS                  | SDDL \_ automático \_ heredado    | \_Se establece la marca de la DACL \_ auto \_ heredada.    |
| "sin \_ control de acceso \_ " | \_ACL null de SSDL \_          | La ACL es NULL.                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_marcas SACL
</dt> <dd>

Marcas de control de descriptor de seguridad que se aplican a la SACL. La cadena de marcas de SACL \_ utiliza las mismas cadenas de bits de control que la cadena de marcas de DACL \_ .

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>ACE de cadena \_
</dt> <dd>

Cadena que describe una ACE en la DACL o SACL del descriptor de seguridad. Para obtener una descripción del formato de cadena ACE, consulte [cadenas ACE](ace-strings.md). Cada cadena ACE se incluye entre paréntesis (()).

</dd> </dl>

Los componentes innecesarios se pueden omitir de la cadena de descriptor de seguridad. Por ejemplo, si \_ \_ no se establece la marca de la DACL de este tipo en el descriptor de seguridad de entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) no incluye un componente D: en la cadena de salida. También puede utilizar las marcas de bits de [**\_ información de seguridad**](security-information.md) para indicar los componentes que se van a incluir en una cadena de descriptor de seguridad.

El formato de cadena de descriptor de seguridad no admite ACL **null** .

Para denotar una ACL vacía, la cadena de descriptor de seguridad incluye el token D: o S: sin información de cadena adicional.

La cadena de descriptor de seguridad almacena los bits de [**control del DEscriptor de seguridad**](security-descriptor-control.md) de maneras diferentes. Los \_ \_ bits presentes de la DACL de se presente o \_ de la SACL \_ se indican mediante la presencia del token D: o S: en la cadena. Otros bits que se aplican a DACL o SACL se almacenan en \_ marcas DACL y en \_ marcas SACL. El propietario de SE ha predeterminado, el grupo de se tiene como valor predeterminado, se \_ \_ \_ \_ \_ \_ ha predeterminado la DACL y los \_ \_ bits con valores predeterminados de SACL no se almacenan en una cadena de descriptor de seguridad. El \_ \_ bit autorelativo de se almacena en la cadena, pero [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) siempre establece este bit en el descriptor de seguridad de salida.

En los ejemplos siguientes se muestran las cadenas de descriptores de seguridad y la información de los descriptores de seguridad asociados.

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

[Lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
