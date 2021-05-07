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
# <a name="security-descriptor-string-format"></a><span data-ttu-id="c049a-103">Formato de cadena del descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="c049a-103">Security Descriptor String Format</span></span>

<span data-ttu-id="c049a-104">El **formato de cadena del descriptor de** seguridad es un formato de texto para almacenar o transportar información en un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c049a-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="c049a-105">Las [**funciones ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usan este formato.</span><span class="sxs-lookup"><span data-stu-id="c049a-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="c049a-106">El formato es una cadena terminada en **NULL** con tokens para indicar cada uno de los cuatro componentes principales de un descriptor de seguridad: owner (O:), primary group (G:), DACL (D:) y SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="c049a-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="c049a-107">[*Las entradas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) y las ACE condicionales tienen formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c049a-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="c049a-108">Para las ACE, consulte [Ace Strings](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="c049a-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="c049a-109">Para las ACE condicionales, vea [Lenguaje de definición de descriptores de seguridad para ACE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)</span><span class="sxs-lookup"><span data-stu-id="c049a-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="c049a-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>sid \_ de propietario</span><span class="sxs-lookup"><span data-stu-id="c049a-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="c049a-111">Cadena [de SID](sid-strings.md) que identifica el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="c049a-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="c049a-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid</span><span class="sxs-lookup"><span data-stu-id="c049a-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="c049a-113">Cadena de SID que identifica el grupo principal del objeto.</span><span class="sxs-lookup"><span data-stu-id="c049a-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="c049a-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>marcas \_ dacl</span><span class="sxs-lookup"><span data-stu-id="c049a-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="c049a-115">Marcas de control del descriptor de seguridad que se aplican a la DACL.</span><span class="sxs-lookup"><span data-stu-id="c049a-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="c049a-116">Para obtener una descripción de estas marcas de control, vea la [**función SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)</span><span class="sxs-lookup"><span data-stu-id="c049a-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="c049a-117">La cadena dacl \_ flags puede ser una concatenación de cero o más de las cadenas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c049a-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="c049a-118">Control</span><span class="sxs-lookup"><span data-stu-id="c049a-118">Control</span></span>               | <span data-ttu-id="c049a-119">Constante en Sddl.h</span><span class="sxs-lookup"><span data-stu-id="c049a-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="c049a-120">Significado</span><span class="sxs-lookup"><span data-stu-id="c049a-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="c049a-121">"P"</span><span class="sxs-lookup"><span data-stu-id="c049a-121">"P"</span></span>                   | <span data-ttu-id="c049a-122">SDDL \_ PROTECTED</span><span class="sxs-lookup"><span data-stu-id="c049a-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="c049a-123">Se establece \_ la marca SE DACL \_ PROTECTED.</span><span class="sxs-lookup"><span data-stu-id="c049a-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="c049a-124">"AR"</span><span class="sxs-lookup"><span data-stu-id="c049a-124">"AR"</span></span>                  | <span data-ttu-id="c049a-125">SDDL \_ AUTO \_ INHERIT \_ REQ</span><span class="sxs-lookup"><span data-stu-id="c049a-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="c049a-126">Se establece \_ la marca SE DACL AUTO INHERIT \_ \_ \_ REQ.</span><span class="sxs-lookup"><span data-stu-id="c049a-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="c049a-127">"IA"</span><span class="sxs-lookup"><span data-stu-id="c049a-127">"AI"</span></span>                  | <span data-ttu-id="c049a-128">SDDL \_ AUTO \_ INHERITED</span><span class="sxs-lookup"><span data-stu-id="c049a-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="c049a-129">Se establece \_ la marca SE DACL AUTO \_ \_ INHERITED.</span><span class="sxs-lookup"><span data-stu-id="c049a-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="c049a-130">"NO \_ ACCESS \_ CONTROL"</span><span class="sxs-lookup"><span data-stu-id="c049a-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="c049a-131">ACL NULL de SDDL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c049a-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="c049a-132">La ACL es null.</span><span class="sxs-lookup"><span data-stu-id="c049a-132">The ACL is null.</span></span> <span data-ttu-id="c049a-133">**Windows Server 2008, Windows Vista y Windows Server 2003:** No disponible.</span><span class="sxs-lookup"><span data-stu-id="c049a-133">**Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c049a-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl \_ flags</span><span class="sxs-lookup"><span data-stu-id="c049a-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="c049a-135">Marcas de control de descriptor de seguridad que se aplican a sacl.</span><span class="sxs-lookup"><span data-stu-id="c049a-135">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="c049a-136">La cadena sacl \_ flags usa las mismas cadenas de bits de control que la cadena dacl \_ flags.</span><span class="sxs-lookup"><span data-stu-id="c049a-136">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="c049a-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace</span><span class="sxs-lookup"><span data-stu-id="c049a-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="c049a-138">Cadena que describe una ACE en la DACL o SACL del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c049a-138">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="c049a-139">Para obtener una descripción del formato de cadena ACE, vea [Ace strings](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="c049a-139">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="c049a-140">Cada cadena ACE se incluye entre paréntesis (()).</span><span class="sxs-lookup"><span data-stu-id="c049a-140">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="c049a-141">Los componentes innecesarios se pueden omitir de la cadena del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c049a-141">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="c049a-142">Por ejemplo, si la marca SE DACL PRESENT no está establecida en el descriptor de seguridad de \_ \_ entrada, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) no incluye un componente D: en la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="c049a-142">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="c049a-143">También puede usar las marcas de bits [**SECURITY \_ INFORMATION**](security-information.md) para indicar los componentes que se incluirán en una cadena de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c049a-143">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="c049a-144">El formato de cadena del descriptor de seguridad no admite **ACL NULL.**</span><span class="sxs-lookup"><span data-stu-id="c049a-144">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="c049a-145">Para indicar una ACL vacía, la cadena del descriptor de seguridad incluye el token D: o S: sin información de cadena adicional.</span><span class="sxs-lookup"><span data-stu-id="c049a-145">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="c049a-146">La cadena de descriptor de seguridad almacena los bits [**DE CONTROL DEL DESCRIPTOR DE SEGURIDAD**](security-descriptor-control.md) de maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="c049a-146">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="c049a-147">Los bits SE DACL PRESENT o SE SACL PRESENT se indican mediante la presencia del \_ \_ token \_ \_ D: o S: en la cadena.</span><span class="sxs-lookup"><span data-stu-id="c049a-147">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="c049a-148">Otros bits que se aplican a la DACL o SACL se almacenan en marcas dacl \_ y \_ sacl.</span><span class="sxs-lookup"><span data-stu-id="c049a-148">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="c049a-149">Los bits SE \_ OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL DEFAULTED y SE \_ \_ SACL DEFAULTED no se almacenan \_ en una cadena de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c049a-149">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="c049a-150">El bit SE SELF RELATIVE no se almacena en la cadena, pero \_ \_ [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) siempre establece este bit en el descriptor de seguridad de salida.</span><span class="sxs-lookup"><span data-stu-id="c049a-150">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="c049a-151">En los ejemplos siguientes se muestran cadenas de descriptores de seguridad y la información de los descriptores de seguridad asociados.</span><span class="sxs-lookup"><span data-stu-id="c049a-151">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="c049a-152">Cadena 1:</span><span class="sxs-lookup"><span data-stu-id="c049a-152">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="c049a-153">Descriptor de seguridad 1:</span><span class="sxs-lookup"><span data-stu-id="c049a-153">Security Descriptor 1:</span></span>


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



<span data-ttu-id="c049a-154">Cadena 2:</span><span class="sxs-lookup"><span data-stu-id="c049a-154">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="c049a-155">Descriptor de seguridad 2:</span><span class="sxs-lookup"><span data-stu-id="c049a-155">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c049a-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c049a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c049a-157">Cadenas ACE</span><span class="sxs-lookup"><span data-stu-id="c049a-157">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="c049a-158">Lenguaje de definición de descriptores de seguridad para A CA condicionales</span><span class="sxs-lookup"><span data-stu-id="c049a-158">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
