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
# <a name="security-descriptor-string-format"></a><span data-ttu-id="1b2c0-103">Formato de cadena de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="1b2c0-103">Security Descriptor String Format</span></span>

<span data-ttu-id="1b2c0-104">El **formato de cadena de descriptor de seguridad** es un formato de texto para almacenar o transportar información en un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="1b2c0-105">Las funciones [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usan este formato.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="1b2c0-106">El formato es una cadena terminada en **null** con tokens para indicar cada uno de los cuatro componentes principales de un descriptor de seguridad: Owner (o:), Primary Group (G:), DACL (D:) y SACL (s:).</span><span class="sxs-lookup"><span data-stu-id="1b2c0-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="1b2c0-107">[*Las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) y las ACE condicionales tienen distintos formatos.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="1b2c0-108">Para las ACE, consulte [cadenas ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="1b2c0-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="1b2c0-109">Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="1b2c0-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="1b2c0-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>SID de propietario \_</span><span class="sxs-lookup"><span data-stu-id="1b2c0-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="1b2c0-111">[Cadena SID](sid-strings.md) que identifica el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="1b2c0-112"><span id="group_sid"></span><span id="GROUP_SID"></span>SID de grupo \_</span><span class="sxs-lookup"><span data-stu-id="1b2c0-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="1b2c0-113">Cadena SID que identifica el grupo primario del objeto.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="1b2c0-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>marcas de DACL \_</span><span class="sxs-lookup"><span data-stu-id="1b2c0-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="1b2c0-115">Marcas de control de descriptor de seguridad que se aplican a la DACL.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="1b2c0-116">Para obtener una descripción de estas marcas de control, consulte la función [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .</span><span class="sxs-lookup"><span data-stu-id="1b2c0-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="1b2c0-117">La \_ cadena de marcas de DACL puede ser una concatenación de cero o más de las siguientes cadenas.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="1b2c0-118">Control</span><span class="sxs-lookup"><span data-stu-id="1b2c0-118">Control</span></span>               | <span data-ttu-id="1b2c0-119">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="1b2c0-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="1b2c0-120">Significado</span><span class="sxs-lookup"><span data-stu-id="1b2c0-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="1b2c0-121">M</span><span class="sxs-lookup"><span data-stu-id="1b2c0-121">"P"</span></span>                   | <span data-ttu-id="1b2c0-122">SDDL \_ protegido</span><span class="sxs-lookup"><span data-stu-id="1b2c0-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="1b2c0-123">\_Se establece la marca protegida de DACL de se \_ .</span><span class="sxs-lookup"><span data-stu-id="1b2c0-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="1b2c0-124">ANALÍTICO</span><span class="sxs-lookup"><span data-stu-id="1b2c0-124">"AR"</span></span>                  | <span data-ttu-id="1b2c0-125">\_solicitud de \_ herencia \_ automática de SDDL</span><span class="sxs-lookup"><span data-stu-id="1b2c0-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="1b2c0-126">\_ \_ \_ Se establece la marca req de herencia automática de DACL de se \_ .</span><span class="sxs-lookup"><span data-stu-id="1b2c0-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="1b2c0-127">EMPLEADOS</span><span class="sxs-lookup"><span data-stu-id="1b2c0-127">"AI"</span></span>                  | <span data-ttu-id="1b2c0-128">SDDL \_ automático \_ heredado</span><span class="sxs-lookup"><span data-stu-id="1b2c0-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="1b2c0-129">\_Se establece la marca de la DACL \_ auto \_ heredada.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="1b2c0-130">"sin \_ control de acceso \_ "</span><span class="sxs-lookup"><span data-stu-id="1b2c0-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="1b2c0-131">\_ACL null de SSDL \_</span><span class="sxs-lookup"><span data-stu-id="1b2c0-131">SSDL\_NULL\_ACL</span></span>          | <span data-ttu-id="1b2c0-132">La ACL es NULL.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="1b2c0-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_marcas SACL</span><span class="sxs-lookup"><span data-stu-id="1b2c0-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="1b2c0-134">Marcas de control de descriptor de seguridad que se aplican a la SACL.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="1b2c0-135">La cadena de marcas de SACL \_ utiliza las mismas cadenas de bits de control que la cadena de marcas de DACL \_ .</span><span class="sxs-lookup"><span data-stu-id="1b2c0-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="1b2c0-136"><span id="string_ace"></span><span id="STRING_ACE"></span>ACE de cadena \_</span><span class="sxs-lookup"><span data-stu-id="1b2c0-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="1b2c0-137">Cadena que describe una ACE en la DACL o SACL del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="1b2c0-138">Para obtener una descripción del formato de cadena ACE, consulte [cadenas ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="1b2c0-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="1b2c0-139">Cada cadena ACE se incluye entre paréntesis (()).</span><span class="sxs-lookup"><span data-stu-id="1b2c0-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="1b2c0-140">Los componentes innecesarios se pueden omitir de la cadena de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="1b2c0-141">Por ejemplo, si \_ \_ no se establece la marca de la DACL de este tipo en el descriptor de seguridad de entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) no incluye un componente D: en la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="1b2c0-142">También puede utilizar las marcas de bits de [**\_ información de seguridad**](security-information.md) para indicar los componentes que se van a incluir en una cadena de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="1b2c0-143">El formato de cadena de descriptor de seguridad no admite ACL **null** .</span><span class="sxs-lookup"><span data-stu-id="1b2c0-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="1b2c0-144">Para denotar una ACL vacía, la cadena de descriptor de seguridad incluye el token D: o S: sin información de cadena adicional.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="1b2c0-145">La cadena de descriptor de seguridad almacena los bits de [**control del DEscriptor de seguridad**](security-descriptor-control.md) de maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="1b2c0-146">Los \_ \_ bits presentes de la DACL de se presente o \_ de la SACL \_ se indican mediante la presencia del token D: o S: en la cadena.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="1b2c0-147">Otros bits que se aplican a DACL o SACL se almacenan en \_ marcas DACL y en \_ marcas SACL.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="1b2c0-148">El propietario de SE ha predeterminado, el grupo de se tiene como valor predeterminado, se \_ \_ \_ \_ \_ \_ ha predeterminado la DACL y los \_ \_ bits con valores predeterminados de SACL no se almacenan en una cadena de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="1b2c0-149">El \_ \_ bit autorelativo de se almacena en la cadena, pero [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) siempre establece este bit en el descriptor de seguridad de salida.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="1b2c0-150">En los ejemplos siguientes se muestran las cadenas de descriptores de seguridad y la información de los descriptores de seguridad asociados.</span><span class="sxs-lookup"><span data-stu-id="1b2c0-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="1b2c0-151">Cadena 1:</span><span class="sxs-lookup"><span data-stu-id="1b2c0-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="1b2c0-152">Descriptor de seguridad 1:</span><span class="sxs-lookup"><span data-stu-id="1b2c0-152">Security Descriptor 1:</span></span>


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



<span data-ttu-id="1b2c0-153">Cadena 2:</span><span class="sxs-lookup"><span data-stu-id="1b2c0-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="1b2c0-154">Descriptor de seguridad 2:</span><span class="sxs-lookup"><span data-stu-id="1b2c0-154">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1b2c0-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b2c0-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b2c0-156">Cadenas ACE</span><span class="sxs-lookup"><span data-stu-id="1b2c0-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="1b2c0-157">Lenguaje de definición de descriptores de seguridad para ACE condicionales</span><span class="sxs-lookup"><span data-stu-id="1b2c0-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
