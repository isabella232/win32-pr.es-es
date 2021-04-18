---
description: Contiene una cláusula de sintaxis que define los datos y el tipo para el objeto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Cláusula de sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707346"
---
# <a name="syntax-clause"></a><span data-ttu-id="c9ab9-103">Cláusula de sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9ab9-103">SYNTAX Clause</span></span>

<span data-ttu-id="c9ab9-104">La macro [Object-Type](object-type-macro.md) contiene una cláusula de sintaxis que define los datos y el tipo para el objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="c9ab9-105">Aunque el proveedor SNMP observa reglas generales para asignar cláusulas de sintaxis, el proveedor también sigue las reglas específicas de varios tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="c9ab9-106">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c9ab9-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="c9ab9-107">Las siguientes reglas de asignación se aplican a todos los tipos de datos descritos en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="c9ab9-108">La representación textual de la cláusula de sintaxis se asigna a la **\_ Convención textual** de la propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="c9ab9-109">La definición de tipo con nombre de la cláusula de sintaxis se asigna a **la \_ Sintaxis de objeto** de calificador de propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="c9ab9-110">Esta asignación difiere en función del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="c9ab9-111">Para obtener más información, vea las descripciones de la asignación.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="c9ab9-112">El tipo de SNMP que se usa al codificar los marcos del protocolo SNMPv1 y SNMPv2C se asigna a la **codificación** del calificador de la propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="c9ab9-113">El calificador de propiedad de CIM **CIMTYPE** contiene la representación textual que da formato al valor del protocolo CIM subyacente.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="c9ab9-114">En la tabla siguiente se enumeran los tipos de datos que tienen reglas específicas que rigen el comportamiento de la asignación de proveedores.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="c9ab9-115">Tipo de datos SNMP</span><span class="sxs-lookup"><span data-stu-id="c9ab9-115">SNMP data type</span></span>                                     | <span data-ttu-id="c9ab9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9ab9-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9ab9-117">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="c9ab9-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="c9ab9-118">Uno de los tipos de datos básicos definidos en la estructura de documentos de información de administración (SMI) RFC 1213 y RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="c9ab9-119">Convención textual</span><span class="sxs-lookup"><span data-stu-id="c9ab9-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="c9ab9-120">Definición de tipo generada mediante el uso explícito de la macro de **Convención de texto** SNMPv2c o generada mediante el uso de un tipo con nombre.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="c9ab9-121">Una Convención textual asigna un nombre y, en algunos casos, un intervalo de valores a un tipo de datos existente.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="c9ab9-122">Tipo con nombre</span><span class="sxs-lookup"><span data-stu-id="c9ab9-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="c9ab9-123">Referencia con nombre a un tipo primitivo, una Convención textual o un tipo restringido.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="c9ab9-124">Tipo restringido</span><span class="sxs-lookup"><span data-stu-id="c9ab9-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="c9ab9-125">Tipo primitivo, tipo con nombre o Convención textual que se ha restringido mediante algún mecanismo de subescritura definido en los documentos de SMI RFC 1213 y RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="c9ab9-126">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="c9ab9-126">Primitive Type</span></span>

<span data-ttu-id="c9ab9-127">El tipo primitivo es uno de los tipos de datos básicos definidos en la estructura de documentos de información de administración (SMI) RFC 1213 y RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="c9ab9-128">Los tipos primitivos SNMP se asignan a los tipos definidos por CIM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="c9ab9-129">En la tabla siguiente se muestra la asignación que se produce cuando la cláusula de sintaxis hace referencia explícitamente a un tipo primitivo para SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="c9ab9-130">Los calificadores de sintaxis de **texto \_**, **codificación** y **\_ Sintaxis de objetos** siempre son los mismos que el tipo de MIB y el valor predeterminado es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="c9ab9-131">Tipo de MIB</span><span class="sxs-lookup"><span data-stu-id="c9ab9-131">MIB type</span></span>         | <span data-ttu-id="c9ab9-132">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-132">CIM variant type</span></span> | <span data-ttu-id="c9ab9-133">valor de CIMTYPE</span><span class="sxs-lookup"><span data-stu-id="c9ab9-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="c9ab9-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="c9ab9-134">INTEGER</span></span>          | <span data-ttu-id="c9ab9-135">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-135">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-136">**sint32**</span></span>    |
| <span data-ttu-id="c9ab9-137">OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="c9ab9-137">OCTETSTRING</span></span>      | <span data-ttu-id="c9ab9-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-138">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-139">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-139">**string**</span></span>    |
| <span data-ttu-id="c9ab9-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="c9ab9-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="c9ab9-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-141">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-142">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-142">**string**</span></span>    |
| <span data-ttu-id="c9ab9-143">NULL</span><span class="sxs-lookup"><span data-stu-id="c9ab9-143">NULL</span></span>             | <span data-ttu-id="c9ab9-144">VT \_ null</span><span class="sxs-lookup"><span data-stu-id="c9ab9-144">VT\_NULL</span></span>         | <span data-ttu-id="c9ab9-145">No compatible</span><span class="sxs-lookup"><span data-stu-id="c9ab9-145">Not supported</span></span> |
| <span data-ttu-id="c9ab9-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="c9ab9-146">IpAddress</span></span>        | <span data-ttu-id="c9ab9-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-147">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-148">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-148">**string**</span></span>    |
| <span data-ttu-id="c9ab9-149">Contador</span><span class="sxs-lookup"><span data-stu-id="c9ab9-149">Counter</span></span>          | <span data-ttu-id="c9ab9-150">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-150">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-151">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-152">Indicador</span><span class="sxs-lookup"><span data-stu-id="c9ab9-152">Gauge</span></span>            | <span data-ttu-id="c9ab9-153">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-153">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-154">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-155">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="c9ab9-155">TimeTicks</span></span>        | <span data-ttu-id="c9ab9-156">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-156">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-157">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-158">Opaca</span><span class="sxs-lookup"><span data-stu-id="c9ab9-158">Opaque</span></span>           | <span data-ttu-id="c9ab9-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-159">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-160">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-160">**string**</span></span>    |
| <span data-ttu-id="c9ab9-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="c9ab9-161">NetworkAddress</span></span>   | <span data-ttu-id="c9ab9-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-162">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-163">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-163">**string**</span></span>    |



 

<span data-ttu-id="c9ab9-164">El proveedor omite la macro OBJECT-TYPE cuando la cláusula de sintaxis hace referencia a **null**, ya sea explícitamente o a través de una asignación de tipo con nombre.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="c9ab9-165">En la tabla siguiente se muestra la asignación que se produce cuando la cláusula de sintaxis hace referencia de forma explícita a un tipo primitivo para SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="c9ab9-166">Los calificadores de sintaxis de **texto \_**, **codificación** y **\_ Sintaxis de objetos** siempre son los mismos que el tipo de MIB y el valor predeterminado es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="c9ab9-167">Tipo de MIB</span><span class="sxs-lookup"><span data-stu-id="c9ab9-167">MIB type</span></span>          | <span data-ttu-id="c9ab9-168">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-168">CIM variant type</span></span> | <span data-ttu-id="c9ab9-169">valor de CIMTYPE</span><span class="sxs-lookup"><span data-stu-id="c9ab9-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="c9ab9-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="c9ab9-170">INTEGER</span></span>           | <span data-ttu-id="c9ab9-171">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-171">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-172">**sint32**</span></span>    |
| <span data-ttu-id="c9ab9-173">CADENA DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="c9ab9-173">OCTET STRING</span></span>      | <span data-ttu-id="c9ab9-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-174">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-175">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-175">**string**</span></span>    |
| <span data-ttu-id="c9ab9-176">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="c9ab9-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="c9ab9-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-177">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-178">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-178">**string**</span></span>    |
| <span data-ttu-id="c9ab9-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="c9ab9-179">IpAddress</span></span>         | <span data-ttu-id="c9ab9-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-180">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-181">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-181">**string**</span></span>    |
| <span data-ttu-id="c9ab9-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="c9ab9-182">Counter32</span></span>         | <span data-ttu-id="c9ab9-183">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-183">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-184">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="c9ab9-185">Gauge32</span></span>           | <span data-ttu-id="c9ab9-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-186">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-187">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="c9ab9-188">Unsigned32</span></span>        | <span data-ttu-id="c9ab9-189">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-189">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-190">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="c9ab9-191">Integer32</span></span>         | <span data-ttu-id="c9ab9-192">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-192">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-193">**sint32**</span></span>    |
| <span data-ttu-id="c9ab9-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="c9ab9-194">Counter64</span></span>         | <span data-ttu-id="c9ab9-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-195">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-196">**uint64**</span></span>    |
| <span data-ttu-id="c9ab9-197">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="c9ab9-197">TimeTicks</span></span>         | <span data-ttu-id="c9ab9-198">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9ab9-198">VT\_I4</span></span>           | <span data-ttu-id="c9ab9-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-199">**uint32**</span></span>    |
| <span data-ttu-id="c9ab9-200">Opaca</span><span class="sxs-lookup"><span data-stu-id="c9ab9-200">Opaque</span></span>            | <span data-ttu-id="c9ab9-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-201">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-202">**string**</span><span class="sxs-lookup"><span data-stu-id="c9ab9-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="c9ab9-203">Tipo con nombre</span><span class="sxs-lookup"><span data-stu-id="c9ab9-203">Named Type</span></span>

<span data-ttu-id="c9ab9-204">Los tipos con nombre SNMP se asignan a los tipos definidos por CIM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="c9ab9-205">Cuando la cláusula de sintaxis hace referencia a un [tipo primitivo](#primitive-type), una [Convención textual](textual-convention-macro.md)o un [tipo restringido](#constrained-type) a través de una derivación de asignación de tipo, use esos tipos para determinar qué procedimientos de asignación se aplican.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="c9ab9-206">Si, mediante la derivación de las reglas de asignación de tipos, encuentra una definición de Tipo restringida:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="c9ab9-207">Y si, a través de la derivación adicional, se encuentra con una de las convenciones de texto enumeradas en [la macro de Convención de texto](textual-convention-macro.md), aplique las reglas de asignación para los tipos y las convenciones de texto restringidos.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="c9ab9-208">De lo contrario, si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipo primitivo, aplique las reglas de asignación para los tipos primitivos y los tipos restringidos.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="c9ab9-209">Si encuentra una de las convenciones de texto enumeradas [en \_ macro de Convención textual](textual-convention-macro.md), aplique las reglas de asignación para las convenciones textuales.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="c9ab9-210">Si encuentra uno de los tipos primitivos enumerados en cualquiera de las tablas de tipo primitivo, aplique las reglas de asignación para los tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="c9ab9-211">Las clases que contienen tipos de propiedad que no se ajustan a la asignación descrita anteriormente no son válidas.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="c9ab9-212">En este caso, el proveedor devuelve un error si y cuando el proveedor solicita la recuperación de una definición de clase al ejecutar una función de recuperación de instancia.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="c9ab9-213">Tipo restringido</span><span class="sxs-lookup"><span data-stu-id="c9ab9-213">Constrained Type</span></span>

<span data-ttu-id="c9ab9-214">Un tipo restringido es un tipo primitivo, un tipo con nombre o una Convención textual que se ha restringido mediante algún mecanismo de subescritura definido en los documentos SMI RFC 1213 y RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="c9ab9-215">Cuando se producen subtipos, se necesitan calificadores CIM adicionales para especificar los valores de subtipo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="c9ab9-216">La definición de tipo con nombre de la cláusula de sintaxis se asigna literalmente a la **\_ Sintaxis de objeto** de calificador de propiedad CIM hasta, pero sin incluir las restricciones del subtipo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="c9ab9-217">Los subtipos pueden seguir cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="c9ab9-218">ENTERO enumerado</span><span class="sxs-lookup"><span data-stu-id="c9ab9-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="c9ab9-219">La **enumeración** de calificador de propiedad CIM especifica los valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="c9ab9-220">Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits firmados.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="c9ab9-221">En la tabla siguiente se enumeran los tipos de asignación.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-221">The following table lists the mapping types.</span></span> <span data-ttu-id="c9ab9-222">El valor predeterminado es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="c9ab9-223">Tipo de MIB restringido</span><span class="sxs-lookup"><span data-stu-id="c9ab9-223">Constrained MIB type</span></span> | <span data-ttu-id="c9ab9-224">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-224">CIM variant type</span></span> | <span data-ttu-id="c9ab9-225">Calificadores CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ab9-226">ENTERO enumerado</span><span class="sxs-lookup"><span data-stu-id="c9ab9-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="c9ab9-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-227">VT\_BSTR</span></span>         | <span data-ttu-id="c9ab9-228">**\_ Convención textual**: enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="c9ab9-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="c9ab9-229">**codificación**: entero</span><span class="sxs-lookup"><span data-stu-id="c9ab9-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="c9ab9-230">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="c9ab9-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="c9ab9-231">BITS</span><span class="sxs-lookup"><span data-stu-id="c9ab9-231">BITS</span></span>

    <span data-ttu-id="c9ab9-232">Los **bits** del calificador de la propiedad CIM especifican los valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="c9ab9-233">Este calificador se representa como una cadena que contiene una lista separada por comas de valores enteros de 32 bits firmados.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="c9ab9-234">En la tabla siguiente se enumeran los tipos de asignación.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-234">The following table lists the mapping types.</span></span> <span data-ttu-id="c9ab9-235">El valor predeterminado es siempre **null**.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="c9ab9-236">Tipo de MIB restringido</span><span class="sxs-lookup"><span data-stu-id="c9ab9-236">Constrained MIB type</span></span> | <span data-ttu-id="c9ab9-237">Tipo de variante CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-237">CIM variant type</span></span>      | <span data-ttu-id="c9ab9-238">Calificadores CIM</span><span class="sxs-lookup"><span data-stu-id="c9ab9-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ab9-239">BITS</span><span class="sxs-lookup"><span data-stu-id="c9ab9-239">BITS</span></span>                 | <span data-ttu-id="c9ab9-240">\_matriz VT \| VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c9ab9-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="c9ab9-241">**\_ Convención textual**: bits</span><span class="sxs-lookup"><span data-stu-id="c9ab9-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="c9ab9-242">**codificación**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="c9ab9-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="c9ab9-243">**CIMTYPE**: cadena</span><span class="sxs-lookup"><span data-stu-id="c9ab9-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="c9ab9-244">Longitud variable</span><span class="sxs-lookup"><span data-stu-id="c9ab9-244">Variable-length</span></span>

    <span data-ttu-id="c9ab9-245">Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como una cadena de octeto de longitud variable u opaca, **la \_ longitud variable** del calificador de propiedad CIM especifica los valores mínimo, máximo y de longitud fija asociados con la definición de tipo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="c9ab9-246">Este calificador se implementa como una cadena en el formato siguiente, donde los valores de longitud variable se representan como enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="c9ab9-247">Longitud fija</span><span class="sxs-lookup"><span data-stu-id="c9ab9-247">Fixed-length</span></span>

    <span data-ttu-id="c9ab9-248">Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como una cadena de octeto de longitud fija o opaca, **la \_ longitud fija** del calificador de propiedad CIM especifica el valor de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="c9ab9-249">Este calificador se representa como un valor entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="c9ab9-250">Intervalo</span><span class="sxs-lookup"><span data-stu-id="c9ab9-250">Range</span></span>

    <span data-ttu-id="c9ab9-251">Cuando la cláusula de sintaxis hace referencia a un tipo primitivo, un tipo con nombre o una Convención textual que se subescribe como un indicador o un entero de valor fijo o de intervalo, el **\_ valor** de la variable de calificador de propiedad CIM especifica los valores de intervalo y fijos asociados a la definición de tipo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="c9ab9-252">Este calificador se implementa como una cadena en el formato siguiente, donde los valores de intervalo y de longitud fija se representan como enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="c9ab9-253">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9ab9-253">Example Code</span></span>

<span data-ttu-id="c9ab9-254">En el siguiente ejemplo se describe un subtipo de entero enumerado.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="c9ab9-255">Este ejemplo se asigna a:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="c9ab9-256">En el ejemplo de código siguiente se describe un subtipo de BITS.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="c9ab9-257">El siguiente ejemplo de código se asigna a:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="c9ab9-258">En el ejemplo de código siguiente se describe un subtipo de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="c9ab9-259">Este ejemplo se asigna a:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="c9ab9-260">En el ejemplo siguiente se describe un subtipo de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="c9ab9-261">Este ejemplo se asigna a:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="c9ab9-262">En el siguiente ejemplo se describe un subtipo de intervalo.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="c9ab9-263">Este ejemplo se asigna a:</span><span class="sxs-lookup"><span data-stu-id="c9ab9-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




