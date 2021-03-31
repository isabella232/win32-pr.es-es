---
description: Explica las cadenas usadas en una entrada de control de acceso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Cadenas ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813291"
---
# <a name="ace-strings"></a><span data-ttu-id="77e61-103">Cadenas ACE</span><span class="sxs-lookup"><span data-stu-id="77e61-103">ACE Strings</span></span>

<span data-ttu-id="77e61-104">El [lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md) (SDDL) utiliza cadenas ACE en los componentes DACL y SACL de una cadena de [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="77e61-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="77e61-105">Como se muestra en los ejemplos de [formato de cadena de descriptor de seguridad](security-descriptor-string-format.md) , cada ACE de una cadena de descriptor de seguridad se incluye entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="77e61-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="77e61-106">Los campos de la ACE están en el siguiente orden y se separan mediante signos de punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="77e61-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="77e61-107">Hay un formato diferente para [*las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) condicionales que otros tipos ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="77e61-108">Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="77e61-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="77e61-109">Campos</span><span class="sxs-lookup"><span data-stu-id="77e61-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="77e61-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo de ACE \_**</span><span class="sxs-lookup"><span data-stu-id="77e61-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-111">Cadena que indica el valor del miembro **AceType** de la estructura del [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="77e61-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="77e61-112">La cadena de tipo ACE puede ser una de las siguientes cadenas definidas en SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="77e61-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="77e61-113">Cadena de tipo ACE</span><span class="sxs-lookup"><span data-stu-id="77e61-113">ACE type string</span></span> | <span data-ttu-id="77e61-114">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="77e61-115">Valor AceType</span><span class="sxs-lookup"><span data-stu-id="77e61-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e61-116">"A"</span><span class="sxs-lookup"><span data-stu-id="77e61-116">"A"</span></span>             | <span data-ttu-id="77e61-117">acceso de SDDL \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="77e61-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="77e61-118">\_tipo de \_ ACE \_ permitido de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="77e61-119">"D"</span><span class="sxs-lookup"><span data-stu-id="77e61-119">"D"</span></span>             | <span data-ttu-id="77e61-120">acceso de SDDL \_ \_ denegado</span><span class="sxs-lookup"><span data-stu-id="77e61-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="77e61-121">tipo de ACE de acceso \_ denegado \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="77e61-122">OA</span><span class="sxs-lookup"><span data-stu-id="77e61-122">"OA"</span></span>            | <span data-ttu-id="77e61-123">\_ \_ acceso a objeto SDDL \_ permitido</span><span class="sxs-lookup"><span data-stu-id="77e61-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="77e61-124">\_tipo de \_ ACE de objeto permitido \_ de acceso \_</span><span class="sxs-lookup"><span data-stu-id="77e61-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="77e61-125">DP</span><span class="sxs-lookup"><span data-stu-id="77e61-125">"OD"</span></span>            | <span data-ttu-id="77e61-126">\_ \_ acceso \_ denegado a objetos SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="77e61-127">tipo de ACE de objeto de acceso \_ denegado \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="77e61-128">ESTÉ</span><span class="sxs-lookup"><span data-stu-id="77e61-128">"AU"</span></span>            | <span data-ttu-id="77e61-129">auditoría de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="77e61-130">\_tipo de \_ ACE de auditoría del sistema \_</span><span class="sxs-lookup"><span data-stu-id="77e61-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="77e61-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="77e61-131">"AL"</span></span>            | <span data-ttu-id="77e61-132">\_alarma SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="77e61-133">\_tipo de \_ ACE de alarma del sistema \_</span><span class="sxs-lookup"><span data-stu-id="77e61-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="77e61-134">ORGANIZA</span><span class="sxs-lookup"><span data-stu-id="77e61-134">"OU"</span></span>            | <span data-ttu-id="77e61-135">\_Auditoría de objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="77e61-136">\_tipo de \_ ACE del objeto de auditoría del sistema \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="77e61-137">OL</span><span class="sxs-lookup"><span data-stu-id="77e61-137">"OL"</span></span>            | <span data-ttu-id="77e61-138">\_alarma de objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="77e61-139">\_tipo de \_ ACE del objeto Alarm \_ del sistema \_</span><span class="sxs-lookup"><span data-stu-id="77e61-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="77e61-140">APROXIMADAMENTE</span><span class="sxs-lookup"><span data-stu-id="77e61-140">"ML"</span></span>            | <span data-ttu-id="77e61-141">\_etiqueta obligatoria de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="77e61-142">\_tipo de \_ ACE de etiqueta obligatoria \_ del sistema \_</span><span class="sxs-lookup"><span data-stu-id="77e61-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="77e61-143">XA</span><span class="sxs-lookup"><span data-stu-id="77e61-143">"XA"</span></span>            | <span data-ttu-id="77e61-144">acceso de devolución de llamada de SDDL \_ \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="77e61-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="77e61-145">\_ \_ \_ \_ Tipo de ACE de devolución **de llamada permitido de acceso windows vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="77e61-146">XD</span><span class="sxs-lookup"><span data-stu-id="77e61-146">"XD"</span></span>            | <span data-ttu-id="77e61-147">\_ \_ acceso denegado de devolución de llamada SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="77e61-148">\_ \_ \_ Tipo de ACE de devolución de llamada de acceso denegado \_ **, windows vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="77e61-149">REMOTA</span><span class="sxs-lookup"><span data-stu-id="77e61-149">"RA"</span></span>            | <span data-ttu-id="77e61-150">\_atributo de recurso SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="77e61-151">\_Tipo de \_ ACE de atributo de recurso del sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="77e61-152">DAÑADO</span><span class="sxs-lookup"><span data-stu-id="77e61-152">"SP"</span></span>            | <span data-ttu-id="77e61-153">identificador de directiva de ámbito de SDDL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="77e61-154">\_ID. de directiva de ámbito del sistema \_ tipo de \_ \_ ACE \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="77e61-155">"XU"</span><span class="sxs-lookup"><span data-stu-id="77e61-155">"XU"</span></span>            | <span data-ttu-id="77e61-156">auditoría de devolución de llamada de SDDL \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="77e61-157">\_Tipo de ACE de devolución de llamada de auditoría del sistema de \_ \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="77e61-158">ZA</span><span class="sxs-lookup"><span data-stu-id="77e61-158">"ZA"</span></span>            | <span data-ttu-id="77e61-159">\_acceso a objetos de devolución de llamada de SDDL \_ \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="77e61-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="77e61-160">\_Tipo de \_ ACE de devolución de llamada permitido de acceso a \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista y Windows Server 2003:** no disponible.</span><span class="sxs-lookup"><span data-stu-id="77e61-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="77e61-161">Si **el \_ tipo ACE** es \_ el tipo de ACE de objeto permitido de acceso y ninguno de los GUID del objeto o el GUID del objeto \_ \_ \_ **heredado \_ \_** tiene un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) especificado, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) convierte el **\_ tipo de ACE** en el tipo de **\_** \_ ACE permitido de acceso \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77e61-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="77e61-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_marcas ACE**</span><span class="sxs-lookup"><span data-stu-id="77e61-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-163">Cadena que indica el valor del miembro **AceFlags** de la estructura del [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="77e61-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="77e61-164">La cadena de marcas ACE puede ser una concatenación de las siguientes cadenas definidas en SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="77e61-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="77e61-165">Cadena de marcas ACE</span><span class="sxs-lookup"><span data-stu-id="77e61-165">ACE flags string</span></span> | <span data-ttu-id="77e61-166">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="77e61-167">Valor AceFlag</span><span class="sxs-lookup"><span data-stu-id="77e61-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="77e61-168">IA</span><span class="sxs-lookup"><span data-stu-id="77e61-168">"CI"</span></span>             | <span data-ttu-id="77e61-169">\_herencia de contenedor de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="77e61-170">\_ACE de herencia de contenedor \_</span><span class="sxs-lookup"><span data-stu-id="77e61-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="77e61-171">OI</span><span class="sxs-lookup"><span data-stu-id="77e61-171">"OI"</span></span>             | <span data-ttu-id="77e61-172">\_herencia de objeto SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="77e61-173">\_ACE de herencia de objeto \_</span><span class="sxs-lookup"><span data-stu-id="77e61-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="77e61-174">PAGINA</span><span class="sxs-lookup"><span data-stu-id="77e61-174">"NP"</span></span>             | <span data-ttu-id="77e61-175">SDDL \_ no \_ Propagate</span><span class="sxs-lookup"><span data-stu-id="77e61-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="77e61-176">NO \_ propagar \_ ACE de herencia \_</span><span class="sxs-lookup"><span data-stu-id="77e61-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="77e61-177">IO</span><span class="sxs-lookup"><span data-stu-id="77e61-177">"IO"</span></span>             | <span data-ttu-id="77e61-178">\_solo herencia de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="77e61-179">solo HEREDAr \_ \_ ACE</span><span class="sxs-lookup"><span data-stu-id="77e61-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="77e61-180">"ID"</span><span class="sxs-lookup"><span data-stu-id="77e61-180">"ID"</span></span>             | <span data-ttu-id="77e61-181">SDDL \_ heredado</span><span class="sxs-lookup"><span data-stu-id="77e61-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="77e61-182">ACE HEREDAda \_</span><span class="sxs-lookup"><span data-stu-id="77e61-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="77e61-183">VALIDA</span><span class="sxs-lookup"><span data-stu-id="77e61-183">"SA"</span></span>             | <span data-ttu-id="77e61-184">auditoría de SDDL \_ \_ correcta</span><span class="sxs-lookup"><span data-stu-id="77e61-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="77e61-185">\_ \_ marca ACE de acceso correcta \_</span><span class="sxs-lookup"><span data-stu-id="77e61-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="77e61-186">REG</span><span class="sxs-lookup"><span data-stu-id="77e61-186">"FA"</span></span>             | <span data-ttu-id="77e61-187">\_error de auditoría de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="77e61-188">\_ \_ marca ACE de acceso con error \_</span><span class="sxs-lookup"><span data-stu-id="77e61-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="77e61-189"><span id="rights"></span><span id="RIGHTS"></span>**necesarios**</span><span class="sxs-lookup"><span data-stu-id="77e61-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-190">Cadena que indica los [derechos de acceso](access-rights-and-access-masks.md) controlados por la ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="77e61-191">Esta cadena puede ser una representación de cadena hexadecimal de los derechos de acceso, como "0x7800003F", o puede ser una concatenación de las siguientes cadenas.</span><span class="sxs-lookup"><span data-stu-id="77e61-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="77e61-192">Derechos de acceso genéricos</span><span class="sxs-lookup"><span data-stu-id="77e61-192">Generic access rights</span></span>

| <span data-ttu-id="77e61-193">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-193">Access rights string</span></span> | <span data-ttu-id="77e61-194">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-194">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-195">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-196">General</span><span class="sxs-lookup"><span data-stu-id="77e61-196">"GA"</span></span>                 | <span data-ttu-id="77e61-197">SDDL \_ genéricos \_</span><span class="sxs-lookup"><span data-stu-id="77e61-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="77e61-198">todos GENÉRICOs \_</span><span class="sxs-lookup"><span data-stu-id="77e61-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="77e61-199">GR</span><span class="sxs-lookup"><span data-stu-id="77e61-199">"GR"</span></span>                 | <span data-ttu-id="77e61-200">\_lectura genérica de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="77e61-201">\_lectura genérica</span><span class="sxs-lookup"><span data-stu-id="77e61-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="77e61-202">GW</span><span class="sxs-lookup"><span data-stu-id="77e61-202">"GW"</span></span>                 | <span data-ttu-id="77e61-203">\_escritura genérica \_ SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="77e61-204">\_escritura genérica</span><span class="sxs-lookup"><span data-stu-id="77e61-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="77e61-205">GX</span><span class="sxs-lookup"><span data-stu-id="77e61-205">"GX"</span></span>                 | <span data-ttu-id="77e61-206">\_ejecución genérica de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="77e61-207">\_ejecución genérica</span><span class="sxs-lookup"><span data-stu-id="77e61-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="77e61-208">Derechos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="77e61-208">Standard access rights</span></span>

| <span data-ttu-id="77e61-209">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-209">Access rights string</span></span> | <span data-ttu-id="77e61-210">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-210">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-211">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-212">CR</span><span class="sxs-lookup"><span data-stu-id="77e61-212">"RC"</span></span>                 | <span data-ttu-id="77e61-213">\_control de lectura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="77e61-214">CONTROL de lectura \_</span><span class="sxs-lookup"><span data-stu-id="77e61-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="77e61-215">DT</span><span class="sxs-lookup"><span data-stu-id="77e61-215">"SD"</span></span>                 | <span data-ttu-id="77e61-216">SDDL \_ estándar de \_ eliminación</span><span class="sxs-lookup"><span data-stu-id="77e61-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="77e61-217">Delete</span><span class="sxs-lookup"><span data-stu-id="77e61-217">DELETE</span></span>          |
| <span data-ttu-id="77e61-218">WD</span><span class="sxs-lookup"><span data-stu-id="77e61-218">"WD"</span></span>                 | <span data-ttu-id="77e61-219">\_DAC de escritura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="77e61-220">ESCRIBIR \_ DAC</span><span class="sxs-lookup"><span data-stu-id="77e61-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="77e61-221">SEM</span><span class="sxs-lookup"><span data-stu-id="77e61-221">"WO"</span></span>                 | <span data-ttu-id="77e61-222">\_propietario de escritura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="77e61-223">propietario de escritura \_</span><span class="sxs-lookup"><span data-stu-id="77e61-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="77e61-224">Derechos de acceso a objetos de servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="77e61-224">Directory service object access rights</span></span>

| <span data-ttu-id="77e61-225">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-225">Access rights string</span></span> | <span data-ttu-id="77e61-226">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-226">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-227">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-228">RP</span><span class="sxs-lookup"><span data-stu-id="77e61-228">"RP"</span></span>                 | <span data-ttu-id="77e61-229">\_propiedad de lectura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="77e61-230">\_right \_ DS \_ leer \_ prop.</span><span class="sxs-lookup"><span data-stu-id="77e61-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="77e61-231">WP</span><span class="sxs-lookup"><span data-stu-id="77e61-231">"WP"</span></span>                 | <span data-ttu-id="77e61-232">\_propiedad de escritura de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="77e61-233">\_prop de \_ \_ escritura DS right de \_ ADS</span><span class="sxs-lookup"><span data-stu-id="77e61-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="77e61-234">CORREOS</span><span class="sxs-lookup"><span data-stu-id="77e61-234">"CC"</span></span>                 | <span data-ttu-id="77e61-235">\_crear \_ elemento secundario de SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="77e61-236">AD \_ derecho \_ DS \_ crear \_ secundario</span><span class="sxs-lookup"><span data-stu-id="77e61-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="77e61-237">CD</span><span class="sxs-lookup"><span data-stu-id="77e61-237">"DC"</span></span>                 | <span data-ttu-id="77e61-238">SDDL \_ eliminar \_ secundario</span><span class="sxs-lookup"><span data-stu-id="77e61-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="77e61-239">ADS \_ derecho \_ DS \_ eliminar \_ secundario</span><span class="sxs-lookup"><span data-stu-id="77e61-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="77e61-240">Live</span><span class="sxs-lookup"><span data-stu-id="77e61-240">"LC"</span></span>                 | <span data-ttu-id="77e61-241">\_ \_ elementos secundarios de la lista SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="77e61-242">AD \_ derecho \_ ACTRL \_ lista de DS \_</span><span class="sxs-lookup"><span data-stu-id="77e61-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="77e61-243">SW</span><span class="sxs-lookup"><span data-stu-id="77e61-243">"SW"</span></span>                 | <span data-ttu-id="77e61-244">\_escritura automática de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="77e61-245">AD \_ right \_ DS \_ Self</span><span class="sxs-lookup"><span data-stu-id="77e61-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="77e61-246">LO</span><span class="sxs-lookup"><span data-stu-id="77e61-246">"LO"</span></span>                  | <span data-ttu-id="77e61-247">\_objeto de lista SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="77e61-248">\_objeto de \_ lista de DS derecho \_ ADS \_</span><span class="sxs-lookup"><span data-stu-id="77e61-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="77e61-249">DT</span><span class="sxs-lookup"><span data-stu-id="77e61-249">"DT"</span></span>                 | <span data-ttu-id="77e61-250">\_árbol de eliminación de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="77e61-251">\_árbol de \_ eliminación de DS derecho \_ de ADS \_</span><span class="sxs-lookup"><span data-stu-id="77e61-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="77e61-252">COMPRA</span><span class="sxs-lookup"><span data-stu-id="77e61-252">"CR"</span></span>                  | <span data-ttu-id="77e61-253">\_acceso de control de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="77e61-254">\_acceso de \_ \_ control DS derecho de \_ ADS</span><span class="sxs-lookup"><span data-stu-id="77e61-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="77e61-255">Derechos de acceso a archivos</span><span class="sxs-lookup"><span data-stu-id="77e61-255">File access rights</span></span>

| <span data-ttu-id="77e61-256">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-256">Access rights string</span></span> | <span data-ttu-id="77e61-257">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-257">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-258">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-259">REG</span><span class="sxs-lookup"><span data-stu-id="77e61-259">"FA"</span></span>                 | <span data-ttu-id="77e61-260">\_ \_ todos los archivos SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="77e61-261">\_acceso a todos los archivos \_</span><span class="sxs-lookup"><span data-stu-id="77e61-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="77e61-262">DIRECCIONA</span><span class="sxs-lookup"><span data-stu-id="77e61-262">"FR"</span></span>                 | <span data-ttu-id="77e61-263">\_lectura de archivo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="77e61-264">lectura de archivo \_ genérico \_</span><span class="sxs-lookup"><span data-stu-id="77e61-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="77e61-265">RV</span><span class="sxs-lookup"><span data-stu-id="77e61-265">"FW"</span></span>                 | <span data-ttu-id="77e61-266">\_escritura de archivos SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="77e61-267">escritura de archivo \_ genérico \_</span><span class="sxs-lookup"><span data-stu-id="77e61-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="77e61-268">EFECTOS</span><span class="sxs-lookup"><span data-stu-id="77e61-268">"FX"</span></span>                 | <span data-ttu-id="77e61-269">\_ejecución de archivo SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="77e61-270">ARCHIVO \_ genérico \_ Execute</span><span class="sxs-lookup"><span data-stu-id="77e61-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="77e61-271">Derechos de acceso de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="77e61-271">Registry key access rights</span></span>

| <span data-ttu-id="77e61-272">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-272">Access rights string</span></span> | <span data-ttu-id="77e61-273">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-273">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-274">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-275">Ka</span><span class="sxs-lookup"><span data-stu-id="77e61-275">"KA"</span></span>                 | <span data-ttu-id="77e61-276">\_ \_ todas las claves SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="77e61-277">acceso de clave \_ \_ a todo</span><span class="sxs-lookup"><span data-stu-id="77e61-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="77e61-278">Corea</span><span class="sxs-lookup"><span data-stu-id="77e61-278">"KR"</span></span>                 | <span data-ttu-id="77e61-279">\_lectura de clave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="77e61-280">lectura de clave \_</span><span class="sxs-lookup"><span data-stu-id="77e61-280">KEY\_READ</span></span>          |
| <span data-ttu-id="77e61-281">KW</span><span class="sxs-lookup"><span data-stu-id="77e61-281">"KW"</span></span>                 | <span data-ttu-id="77e61-282">\_escritura de claves SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="77e61-283">escritura de claves \_</span><span class="sxs-lookup"><span data-stu-id="77e61-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="77e61-284">KX</span><span class="sxs-lookup"><span data-stu-id="77e61-284">"KX"</span></span>                 | <span data-ttu-id="77e61-285">\_ejecución de clave SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="77e61-286">ejecución de clave \_</span><span class="sxs-lookup"><span data-stu-id="77e61-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="77e61-287">Derechos de etiqueta obligatorios</span><span class="sxs-lookup"><span data-stu-id="77e61-287">Mandatory label rights</span></span>

| <span data-ttu-id="77e61-288">Cadena de derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-288">Access rights string</span></span> | <span data-ttu-id="77e61-289">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-289">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-290">Valor derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="77e61-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="77e61-291">Nr</span><span class="sxs-lookup"><span data-stu-id="77e61-291">"NR"</span></span>                 | <span data-ttu-id="77e61-292">SDDL \_ no \_ lectura \_</span><span class="sxs-lookup"><span data-stu-id="77e61-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="77e61-293">NO se ha leído la \_ etiqueta obligatoria del sistema \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="77e61-294">NOROESTE</span><span class="sxs-lookup"><span data-stu-id="77e61-294">"NW"</span></span>                 | <span data-ttu-id="77e61-295">\_no \_ escribir SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="77e61-296">\_no se \_ ha \_ \_ configurado ninguna \_ etiqueta obligatoria del sistema</span><span class="sxs-lookup"><span data-stu-id="77e61-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="77e61-297">NX</span><span class="sxs-lookup"><span data-stu-id="77e61-297">"NX"</span></span>                 | <span data-ttu-id="77e61-298">SDDL \_ no \_ ejecutar \_</span><span class="sxs-lookup"><span data-stu-id="77e61-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="77e61-299">NO se ha ejecutado la \_ etiqueta obligatoria del sistema \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="77e61-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="77e61-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID del objeto \_**</span><span class="sxs-lookup"><span data-stu-id="77e61-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-301">Representación de cadena de un GUID que indica el valor del miembro **objecttype** de una estructura ACE específica del objeto, como [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="77e61-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="77e61-302">La cadena GUID usa el formato devuelto por la función [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="77e61-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="77e61-303">En la tabla siguiente se enumeran algunos GUID de objetos de uso frecuente.</span><span class="sxs-lookup"><span data-stu-id="77e61-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="77e61-304">Derechos y GUID</span><span class="sxs-lookup"><span data-stu-id="77e61-304">Rights and GUID</span></span>                         | <span data-ttu-id="77e61-305">Permiso</span><span class="sxs-lookup"><span data-stu-id="77e61-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="77e61-306">CR; ab721a53-1e2f-11d0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="77e61-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="77e61-307">Cambiar contraseña</span><span class="sxs-lookup"><span data-stu-id="77e61-307">Change password</span></span> |
| <span data-ttu-id="77e61-308">CR; 00299570-246d-11d0-A768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="77e61-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="77e61-309">Restablecimiento de contraseña</span><span class="sxs-lookup"><span data-stu-id="77e61-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="77e61-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**heredar \_ GUID del objeto \_**</span><span class="sxs-lookup"><span data-stu-id="77e61-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-311">Representación de cadena de un GUID que indica el valor del miembro **InheritedObjectType** de una estructura ACE específica del objeto.</span><span class="sxs-lookup"><span data-stu-id="77e61-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="77e61-312">La cadena GUID usa el formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .</span><span class="sxs-lookup"><span data-stu-id="77e61-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="77e61-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**SID de cuenta \_**</span><span class="sxs-lookup"><span data-stu-id="77e61-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-314">[Cadena SID](sid-strings.md) que identifica el [Administrador de confianza](trustees.md) de la ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="77e61-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**atributo de recurso \_**</span><span class="sxs-lookup"><span data-stu-id="77e61-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="77e61-316">\[OPCIONAL \] el \_ atributo de recurso es solo para las ACE de recursos y es opcional.</span><span class="sxs-lookup"><span data-stu-id="77e61-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="77e61-317">Cadena que indica el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="77e61-317">A string that indicates the data type.</span></span> <span data-ttu-id="77e61-318">El tipo de datos ACE del atributo de recurso puede ser uno de los siguientes tipos de datos definidos en SDDL. h.</span><span class="sxs-lookup"><span data-stu-id="77e61-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="77e61-319">El \# signo "" es sinónimo de "0" en los atributos de recursos.</span><span class="sxs-lookup"><span data-stu-id="77e61-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="77e61-320">Por ejemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) es equivalente a e interpretado como D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="77e61-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="77e61-321">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista y Windows server 2003:** Los atributos de recursos no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="77e61-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="77e61-322">Cadena de tipo de datos ACE de atributo de recurso</span><span class="sxs-lookup"><span data-stu-id="77e61-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="77e61-323">Constante en SDDL. h</span><span class="sxs-lookup"><span data-stu-id="77e61-323">Constant in Sddl.h</span></span> | <span data-ttu-id="77e61-324">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="77e61-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="77e61-325">TI</span><span class="sxs-lookup"><span data-stu-id="77e61-325">"TI"</span></span>                                    | <span data-ttu-id="77e61-326">SDDL \_ int</span><span class="sxs-lookup"><span data-stu-id="77e61-326">SDDL\_INT</span></span>          | <span data-ttu-id="77e61-327">Entero con signo</span><span class="sxs-lookup"><span data-stu-id="77e61-327">Signed integer</span></span>   |
| <span data-ttu-id="77e61-328">TU</span><span class="sxs-lookup"><span data-stu-id="77e61-328">"TU"</span></span>                                    | <span data-ttu-id="77e61-329">SDDL ( \_ uint)</span><span class="sxs-lookup"><span data-stu-id="77e61-329">SDDL\_UINT</span></span>         | <span data-ttu-id="77e61-330">Entero sin signo</span><span class="sxs-lookup"><span data-stu-id="77e61-330">Unsigned integer</span></span> |
| <span data-ttu-id="77e61-331">TS</span><span class="sxs-lookup"><span data-stu-id="77e61-331">"TS"</span></span>                                    | <span data-ttu-id="77e61-332">\_WSTRING SDDL</span><span class="sxs-lookup"><span data-stu-id="77e61-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="77e61-333">Cadena ancha</span><span class="sxs-lookup"><span data-stu-id="77e61-333">Wide string</span></span>      |
| <span data-ttu-id="77e61-334">TD</span><span class="sxs-lookup"><span data-stu-id="77e61-334">"TD"</span></span>                                    | <span data-ttu-id="77e61-335">SID de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-335">SDDL\_SID</span></span>          | <span data-ttu-id="77e61-336">SID</span><span class="sxs-lookup"><span data-stu-id="77e61-336">SID</span></span>              |
| <span data-ttu-id="77e61-337">TX</span><span class="sxs-lookup"><span data-stu-id="77e61-337">"TX"</span></span>                                    | <span data-ttu-id="77e61-338">BLOB de SDDL \_</span><span class="sxs-lookup"><span data-stu-id="77e61-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="77e61-339">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="77e61-339">Octet string</span></span>     |
| <span data-ttu-id="77e61-340">TB</span><span class="sxs-lookup"><span data-stu-id="77e61-340">"TB"</span></span>                                    | <span data-ttu-id="77e61-341">SDDL \_ booleano</span><span class="sxs-lookup"><span data-stu-id="77e61-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="77e61-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="77e61-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="77e61-343">En el ejemplo siguiente se muestra una cadena ACE para una ACE con acceso permitido.</span><span class="sxs-lookup"><span data-stu-id="77e61-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="77e61-344">No es una ACE específica del objeto, por lo que no tiene información en los **campos \_ GUID** del objeto y **heredar \_ \_ GUID del objeto** .</span><span class="sxs-lookup"><span data-stu-id="77e61-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="77e61-345">El **campo \_ marcas ACE** también está vacío, lo que indica que no se ha establecido ninguna de las marcas ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="77e61-346">La cadena ACE mostrada anteriormente describe la siguiente información de ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="77e61-347">En el ejemplo siguiente se muestra un archivo clasificado con notificaciones de recursos para Windows y Lenguaje de consulta estructurado (SQL) con la confidencialidad establecida en alto impacto empresarial.</span><span class="sxs-lookup"><span data-stu-id="77e61-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="77e61-348">La cadena ACE mostrada anteriormente describe la siguiente información de ACE.</span><span class="sxs-lookup"><span data-stu-id="77e61-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="77e61-349">Para obtener más información, vea [formato de cadena de descriptor de seguridad](security-descriptor-string-format.md) y cadenas de [SID](sid-strings.md).</span><span class="sxs-lookup"><span data-stu-id="77e61-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="77e61-350">Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="77e61-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e61-351">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77e61-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="77e61-352">[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="77e61-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

