---
description: Las convenciones de texto de SNMP se asignan a tipos definidos por CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de Convención de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706031"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="4fe9b-103">Macro de Convención de texto</span><span class="sxs-lookup"><span data-stu-id="4fe9b-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="4fe9b-104">Las convenciones de texto de SNMP se asignan a tipos definidos por CIM.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="4fe9b-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4fe9b-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="4fe9b-106">Las siguientes reglas de asignación se aplican a las convenciones de texto de SNMP:</span><span class="sxs-lookup"><span data-stu-id="4fe9b-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="4fe9b-107">La definición de tipo con nombre de la cláusula de sintaxis se asigna literalmente a **la \_ Sintaxis de objeto** de calificador de propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="4fe9b-108">Use la tabla siguiente para asignar convenciones de texto cuando la cláusula de sintaxis hace referencia de forma explícita a una Convención textual de una macro de Convención de texto SNMPv2C o hace referencia a una Convención textual implícita.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="4fe9b-109">El valor predeterminado es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="4fe9b-110">Convención textual</span><span class="sxs-lookup"><span data-stu-id="4fe9b-110">Textual convention</span></span> | <span data-ttu-id="4fe9b-111">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="4fe9b-111">CIM variant type</span></span> | <span data-ttu-id="4fe9b-112">Calificador de CIM</span><span class="sxs-lookup"><span data-stu-id="4fe9b-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe9b-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="4fe9b-113">DateAndTime</span></span>        | <span data-ttu-id="4fe9b-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-115">**\_ Convención textual**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="4fe9b-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="4fe9b-116">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-117">**\_ Sintaxis de objeto**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="4fe9b-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="4fe9b-118">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="4fe9b-119">Displaystring</span><span class="sxs-lookup"><span data-stu-id="4fe9b-119">Displaystring</span></span>      | <span data-ttu-id="4fe9b-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-121">**\_ Convención textual**: Displaystring</span><span class="sxs-lookup"><span data-stu-id="4fe9b-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="4fe9b-122">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-123">**\_ Sintaxis de objeto**: Displaystring</span><span class="sxs-lookup"><span data-stu-id="4fe9b-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="4fe9b-124">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="4fe9b-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-125">MacAddress</span></span>         | <span data-ttu-id="4fe9b-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-127">**\_ Convención textual**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="4fe9b-128">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-129">**\_ Sintaxis de objeto**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="4fe9b-130">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="4fe9b-131">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-131">PhysAddress</span></span>        | <span data-ttu-id="4fe9b-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-133">**\_ Convención textual**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="4fe9b-134">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-135">**\_ Sintaxis de objeto**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="4fe9b-136">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="4fe9b-137">SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="4fe9b-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-139">**\_ Convención textual**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="4fe9b-140">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-141">**\_ Sintaxis de objeto**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="4fe9b-142">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="4fe9b-143">SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="4fe9b-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-145">**\_ Convención textual**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="4fe9b-146">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-147">**\_ Sintaxis de objeto**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="4fe9b-148">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="4fe9b-149">SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="4fe9b-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="4fe9b-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="4fe9b-151">**\_ Convención textual**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="4fe9b-152">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="4fe9b-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="4fe9b-153">**\_ Sintaxis de objeto**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="4fe9b-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="4fe9b-154">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="4fe9b-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="4fe9b-155">El tipo Variant definido por CIM y los calificadores de propiedad CIM, la **\_ Convención textual**, la **codificación**, la **\_ Sintaxis de objeto** y la asignación **CIMTYPE** mediante el tipo primitivo subyacente.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="4fe9b-156">La cláusula DISPLAY-HINT de la macro de Convención de texto SNMPv2C se asigna literalmente a la **\_ sugerencia de presentación** del calificador de propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="4fe9b-157">Este calificador no se genera si no hay ninguna macro de Convención de texto o la macro no contiene una cláusula de sugerencia de presentación.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="4fe9b-158">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4fe9b-158">Example Code</span></span>

<span data-ttu-id="4fe9b-159">En el siguiente ejemplo se describe una Convención textual de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="4fe9b-160">Este ejemplo genera los siguientes calificadores CIM.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="4fe9b-161">En el siguiente ejemplo se describe una Convención textual de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="4fe9b-162">Este ejemplo genera los siguientes calificadores CIM.</span><span class="sxs-lookup"><span data-stu-id="4fe9b-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




