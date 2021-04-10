---
description: La macro OBJECT-TYPE contiene cláusulas obligatorias y opcionales que describen las características básicas de un objeto MIB. El proveedor SNMP convierte una MIB en las partes correspondientes de la macro OBJECT-TYPE.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro OBJECT-TYPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153726"
---
# <a name="object-type-macro"></a><span data-ttu-id="6b433-104">Macro OBJECT-TYPE</span><span class="sxs-lookup"><span data-stu-id="6b433-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="6b433-105">La macro OBJECT-TYPE contiene cláusulas obligatorias y opcionales que describen las características básicas de un objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="6b433-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="6b433-106">El proveedor SNMP convierte una MIB en las partes correspondientes de la macro OBJECT-TYPE.</span><span class="sxs-lookup"><span data-stu-id="6b433-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="6b433-107">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6b433-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="6b433-108">Componentes</span><span class="sxs-lookup"><span data-stu-id="6b433-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="6b433-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB (objeto)</span><span class="sxs-lookup"><span data-stu-id="6b433-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="6b433-110">Objeto que contiene la mayoría de los datos en cuestión.</span><span class="sxs-lookup"><span data-stu-id="6b433-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descriptor de objeto</span><span class="sxs-lookup"><span data-stu-id="6b433-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="6b433-112">Nombre único o descriptor de objeto que identifica cada objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="6b433-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="6b433-113">Cada descriptor de objeto MIB asigna exactamente a un nombre de propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="6b433-114">Por **ejemplo, el** **siguiente se convierte** en un bajo.</span><span class="sxs-lookup"><span data-stu-id="6b433-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Cláusula de sintaxis](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="6b433-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="6b433-116">Define los datos y el tipo de un objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="6b433-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX (cláusula)](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="6b433-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="6b433-118">Define una clave para seleccionar una fila de tabla única.</span><span class="sxs-lookup"><span data-stu-id="6b433-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUMENTA la cláusula</span><span class="sxs-lookup"><span data-stu-id="6b433-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-120">Indica que la colección de tablas que especifica se puede considerar una extensión de otra colección de tablas y puede reemplazar la cláusula INDEX en SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="6b433-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="6b433-121">Las colecciones a las que hace referencia la cláusula INCREMENTs se pueden combinar con la otra colección de tablas para formar una colección.</span><span class="sxs-lookup"><span data-stu-id="6b433-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="6b433-122">La colección resultante comparte las propiedades de clave principal especificadas en la última colección de tablas de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6b433-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="6b433-123">En este caso, las reglas de asignación anteriores especificadas para la cláusula INDEX se aplican a la última colección de tablas de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6b433-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="6b433-124">A continuación, la colección de objetos se asigna a una definición de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-Identifier (cláusula)</span><span class="sxs-lookup"><span data-stu-id="6b433-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-126">Contiene un identificador de objeto único para un objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="6b433-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="6b433-127">Este identificador de objeto se asigna al **\_ identificador de objeto** del calificador de la propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Cláusulas Access y MAX-ACCESS](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="6b433-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="6b433-129">Defina los derechos de acceso al objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="6b433-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula Description</span><span class="sxs-lookup"><span data-stu-id="6b433-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-131">Proporciona una descripción de texto del objeto, que se asigna a la **Descripción** del calificador de la propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="6b433-132">Esta cláusula puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="6b433-132">This clause may be empty.</span></span>

<span data-ttu-id="6b433-133">Cada objeto de **tabla** y **entrada** de una definición de tabla SNMP también contiene una cláusula de descripción, que también puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="6b433-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="6b433-134">Las cláusulas de descripción de tabla y entrada se concatenan y el resultado se asigna a la **Descripción** del calificador de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUs (cláusula)</span><span class="sxs-lookup"><span data-stu-id="6b433-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-136">Indica si se debe admitir el objeto.</span><span class="sxs-lookup"><span data-stu-id="6b433-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="6b433-137">Cuando el valor de la cláusula STATUs es **obsoleto**, el proveedor descarta el objeto MIB de la asignación.</span><span class="sxs-lookup"><span data-stu-id="6b433-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="6b433-138">De lo contrario, la cláusula STATUs se asigna al **Estado** del calificador de la propiedad CIM.</span><span class="sxs-lookup"><span data-stu-id="6b433-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="6b433-139">Para SNMPv1, el valor preferido de **status** es **obligatorio** u **opcional**, pero el calificador puede contener algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="6b433-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="6b433-140">Para SNMPv2C, el valor preferido de **status** es **Current** u **deprecated**, pero el calificador puede contener algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="6b433-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL, cláusula</span><span class="sxs-lookup"><span data-stu-id="6b433-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-142">Asigna un valor predeterminado a una variable en una fila de tabla lógica y se asigna al calificador de la propiedad CIM de cadena **Defval**.</span><span class="sxs-lookup"><span data-stu-id="6b433-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula REFERENCE</span><span class="sxs-lookup"><span data-stu-id="6b433-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-144">Hace referencia a otro documento que contiene más información sobre el objeto.</span><span class="sxs-lookup"><span data-stu-id="6b433-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="6b433-145">Esta cláusula se asigna a la **referencia** de calificador de la propiedad CIM, que es de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="6b433-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="6b433-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITs (cláusula)</span><span class="sxs-lookup"><span data-stu-id="6b433-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="6b433-147">Proporciona una definición precisa de lo que representa el objeto.</span><span class="sxs-lookup"><span data-stu-id="6b433-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="6b433-148">Esta cláusula se asigna a las **unidades** de calificador de la propiedad CIM, que es de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="6b433-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b433-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b433-149">Remarks</span></span>

<span data-ttu-id="6b433-150">La macro OBJECT-TYPE describe las características básicas de un objeto MIB individual.</span><span class="sxs-lookup"><span data-stu-id="6b433-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="6b433-151">Un conjunto de macros de tipo de objeto se puede considerar como un grupo de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="6b433-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="6b433-152">En SNMPv2C, utilice la macro OBJECT-GROUP para agrupar formalmente conjuntos de objetos relacionados en una colección.</span><span class="sxs-lookup"><span data-stu-id="6b433-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="6b433-153">Sin embargo, no hay ningún mecanismo formal para crear colecciones en SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="6b433-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="6b433-154">En el caso del proveedor SNMP, se omite la macro de grupo de objetos, pero puede inventar las relaciones y agrupar las colecciones.</span><span class="sxs-lookup"><span data-stu-id="6b433-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



