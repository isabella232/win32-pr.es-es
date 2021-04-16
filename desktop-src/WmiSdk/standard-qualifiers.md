---
description: Todas las implementaciones compatibles con CIM deben controlar un conjunto estándar de calificadores.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Calificadores estándar
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706080"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="504f0-103">Calificadores estándar</span><span class="sxs-lookup"><span data-stu-id="504f0-103">Standard Qualifiers</span></span>

<span data-ttu-id="504f0-104">Todas las implementaciones compatibles con CIM deben controlar un conjunto estándar de calificadores.</span><span class="sxs-lookup"><span data-stu-id="504f0-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="504f0-105">Cualquier objeto específico no tiene todos los calificadores enumerados.</span><span class="sxs-lookup"><span data-stu-id="504f0-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="504f0-106">Normalmente, las clases de extensión proporcionan calificadores adicionales para facilitar el aprovisionamiento de instancias de clase y otras operaciones en la clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="504f0-107">Es responsabilidad del proveedor aplicar los calificadores.</span><span class="sxs-lookup"><span data-stu-id="504f0-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="504f0-108">WMI no aplica calificadores, pero solo los utiliza para informar al usuario sobre cómo se usa la propiedad.</span><span class="sxs-lookup"><span data-stu-id="504f0-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="504f0-109">WMI es compatible con la especificación CIM 2,5.</span><span class="sxs-lookup"><span data-stu-id="504f0-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="504f0-110">Los calificadores tienen las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="504f0-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="504f0-111">No todos los calificadores estándar se pueden usar juntos.</span><span class="sxs-lookup"><span data-stu-id="504f0-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="504f0-112">No todos los calificadores se pueden aplicar a todas las construcciones, como Association o Reference.</span><span class="sxs-lookup"><span data-stu-id="504f0-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="504f0-113">Estas limitaciones se identifican en la lista se aplica a.</span><span class="sxs-lookup"><span data-stu-id="504f0-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="504f0-114">Para una construcción determinada, como Association o Reference, el uso de los calificadores legales se puede restringir aún más porque algunos calificadores son mutuamente excluyentes, el uso de un calificador puede implicar algunas restricciones en el valor de otro, etc.</span><span class="sxs-lookup"><span data-stu-id="504f0-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="504f0-115">Estas reglas de uso están documentadas.</span><span class="sxs-lookup"><span data-stu-id="504f0-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="504f0-116">Los calificadores válidos son heredados por entidades como propiedades, métodos, instancias o subclases únicamente, no por asociaciones ni referencias.</span><span class="sxs-lookup"><span data-stu-id="504f0-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="504f0-117">Por ejemplo, las referencias no heredan el calificador **MaxLen** que se aplica a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="504f0-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="504f0-118">A continuación se enumeran los calificadores estándar de WMI.</span><span class="sxs-lookup"><span data-stu-id="504f0-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="504f0-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="504f0-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-120">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-121">Se aplica a: clases, asociaciones, indicaciones</span><span class="sxs-lookup"><span data-stu-id="504f0-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="504f0-122">Indica si la clase es abstracta y solo sirve como base para las nuevas clases.</span><span class="sxs-lookup"><span data-stu-id="504f0-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="504f0-123">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-123">The default is **FALSE**.</span></span> <span data-ttu-id="504f0-124">No se pueden crear instancias de clases abstractas.</span><span class="sxs-lookup"><span data-stu-id="504f0-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="504f0-125">La ausencia de este calificador indica que la clase no es abstracta; por lo tanto, este calificador es necesario para todas las clases abstractas.</span><span class="sxs-lookup"><span data-stu-id="504f0-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Agregado**</span><span class="sxs-lookup"><span data-stu-id="504f0-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-127">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-128">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-128">Applies to: references</span></span>

<span data-ttu-id="504f0-129">Indica si la referencia es el componente primario de una asociación de agregación.</span><span class="sxs-lookup"><span data-stu-id="504f0-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="504f0-130">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-130">The default is **FALSE**.</span></span>

<span data-ttu-id="504f0-131">Uso: los **calificadores de agregación y** **agregado** se usan juntos la   **agregación** califica la asociación y **Aggregate** especifica la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="504f0-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Concentrado**</span><span class="sxs-lookup"><span data-stu-id="504f0-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-133">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-134">Se aplica a: asociaciones</span><span class="sxs-lookup"><span data-stu-id="504f0-134">Applies to: associations</span></span>

<span data-ttu-id="504f0-135">Indica si la asociación es una agregación.</span><span class="sxs-lookup"><span data-stu-id="504f0-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="504f0-136">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-136">The default is **FALSE**.</span></span> <span data-ttu-id="504f0-137">Se utiliza con **Aggregate**.</span><span class="sxs-lookup"><span data-stu-id="504f0-137">Used with **Aggregate**.</span></span> <span data-ttu-id="504f0-138">Este calificador es necesario para todas las asociaciones de agregación.</span><span class="sxs-lookup"><span data-stu-id="504f0-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span><span class="sxs-lookup"><span data-stu-id="504f0-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-140">Data type: **string**</span></span>

<span data-ttu-id="504f0-141">Se aplica a: propiedades, referencias, métodos</span><span class="sxs-lookup"><span data-stu-id="504f0-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="504f0-142">Nombre alternativo para una propiedad o un método en el esquema.</span><span class="sxs-lookup"><span data-stu-id="504f0-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="504f0-143">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="504f0-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-145">Data type: **string**</span></span>

<span data-ttu-id="504f0-146">Se aplica a: propiedades, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="504f0-147">Tipo de la matriz calificada.</span><span class="sxs-lookup"><span data-stu-id="504f0-147">Type of the qualified array.</span></span>

<span data-ttu-id="504f0-148">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="504f0-148">Valid values are:</span></span>

-   <span data-ttu-id="504f0-149">bolsa (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="504f0-149">bag (default)</span></span>
-   <span data-ttu-id="504f0-150">indizadas</span><span class="sxs-lookup"><span data-stu-id="504f0-150">indexed</span></span>
-   <span data-ttu-id="504f0-151">ordered</span><span class="sxs-lookup"><span data-stu-id="504f0-151">ordered</span></span>

<span data-ttu-id="504f0-152">Uso: aplique este tipo de calificador solo a las propiedades y los parámetros que son matrices (definidas mediante la sintaxis de paréntesis).</span><span class="sxs-lookup"><span data-stu-id="504f0-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="504f0-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**MyBitmap**</span><span class="sxs-lookup"><span data-stu-id="504f0-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-154">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-154">Data type: **string array**</span></span>

<span data-ttu-id="504f0-155">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-156">Asignación de posiciones de bits significativas en las que cada posición significativa puede ser "ON" u "OFF".</span><span class="sxs-lookup"><span data-stu-id="504f0-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="504f0-157">Cada bit "ON" se asigna a un valor correspondiente en la matriz **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="504f0-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="504f0-158">Al tener varios bits "ON", se indican varios valores simultáneos en la matriz **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="504f0-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="504f0-159">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-159">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-160">Para obtener más información, consulte [Bitmap y BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="504f0-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="504f0-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span><span class="sxs-lookup"><span data-stu-id="504f0-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-162">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-162">Data type: **string array**</span></span>

<span data-ttu-id="504f0-163">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-164">Traducción de un valor de posición de bits en una **cadena** asociada.</span><span class="sxs-lookup"><span data-stu-id="504f0-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="504f0-165">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-165">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-166">Para obtener más información, consulte [Bitmap y BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="504f0-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="504f0-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span><span class="sxs-lookup"><span data-stu-id="504f0-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-168">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-169">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="504f0-169">Applies to: methods</span></span>

<span data-ttu-id="504f0-170">Indica si el método crea instancias de.</span><span class="sxs-lookup"><span data-stu-id="504f0-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="504f0-171">Estos métodos no están restringidos a actuar en una sola instancia o en una sola clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="504f0-172">Por ejemplo, un constructor puede crear instancias de asociación, así como instancias de la clase que define el constructor.</span><span class="sxs-lookup"><span data-stu-id="504f0-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="504f0-173">El calificador de **constructor** está pensado únicamente para información y no se espera que lo actúe el administrador de objetos.</span><span class="sxs-lookup"><span data-stu-id="504f0-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="504f0-174">El administrador de objetos no tiene que llamar a métodos de constructor cuando se crea un objeto.</span><span class="sxs-lookup"><span data-stu-id="504f0-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="504f0-175">Además, cuando se llama a un constructor, el administrador de objetos no tiene que invocar ningún método de constructor definido para cualquier clase primaria de la clase original.</span><span class="sxs-lookup"><span data-stu-id="504f0-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="504f0-176">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span><span class="sxs-lookup"><span data-stu-id="504f0-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-178">Data type: **string**</span></span>

<span data-ttu-id="504f0-179">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-179">Applies to: classes</span></span>

<span data-ttu-id="504f0-180">Nombre del método por el que se crean las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="504f0-181">El valor es "PutInstance" o el nombre de otro método que crea las instancias.</span><span class="sxs-lookup"><span data-stu-id="504f0-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="504f0-182">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-182">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-183">Uso: este calificador solo se puede usar si el calificador **SupportsCreate** está presente.</span><span class="sxs-lookup"><span data-stu-id="504f0-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span><span class="sxs-lookup"><span data-stu-id="504f0-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-185">Data type: **string**</span></span>

<span data-ttu-id="504f0-186">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-186">Applies to: classes</span></span>

<span data-ttu-id="504f0-187">Nombre del método por el que se eliminan las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="504f0-188">El valor es "DeleteInstance" o el nombre de otro método que elimina las instancias.</span><span class="sxs-lookup"><span data-stu-id="504f0-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="504f0-189">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-189">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-190">Uso: este calificador solo se puede usar si el calificador **SupportsDelete** está presente.</span><span class="sxs-lookup"><span data-stu-id="504f0-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="504f0-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-192">Data type: **string**</span></span>

<span data-ttu-id="504f0-193">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="504f0-193">Applies to: any</span></span>

<span data-ttu-id="504f0-194">Descripción de un elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="504f0-194">Description of a named element.</span></span> <span data-ttu-id="504f0-195">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span><span class="sxs-lookup"><span data-stu-id="504f0-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-197">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-197">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-198">Se aplica a: métodos</span><span class="sxs-lookup"><span data-stu-id="504f0-198">Applies to: methods</span></span>

<span data-ttu-id="504f0-199">Indica si el método elimina instancias.</span><span class="sxs-lookup"><span data-stu-id="504f0-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="504f0-200">Los métodos que usan el calificador de **destructor** eliminan las instancias a las que se aplica el destructor y no están restringidas a actuar en una sola instancia o clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="504f0-201">Por ejemplo, un destructor podría eliminar las instancias de asociación, así como las instancias de la clase que define el destructor.</span><span class="sxs-lookup"><span data-stu-id="504f0-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="504f0-202">El calificador de **destructor** está pensado únicamente para la información y no se espera que lo actúe el administrador de objetos.</span><span class="sxs-lookup"><span data-stu-id="504f0-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="504f0-203">El administrador de objetos no tiene ninguna obligación de llamar a un método que tiene el calificador de **destructor** cuando se elimina una instancia.</span><span class="sxs-lookup"><span data-stu-id="504f0-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="504f0-204">Además, cuando se llama a un destructor, el administrador de objetos no tiene que invocar los métodos de destructor definidos para cualquier clase primaria de la clase original.</span><span class="sxs-lookup"><span data-stu-id="504f0-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="504f0-205">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="504f0-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-207">Data type: **string**</span></span>

<span data-ttu-id="504f0-208">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="504f0-208">Applies to: any</span></span>

<span data-ttu-id="504f0-209">Nombre que se muestra en la interfaz de usuario en lugar del nombre real del elemento.</span><span class="sxs-lookup"><span data-stu-id="504f0-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="504f0-210">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span><span class="sxs-lookup"><span data-stu-id="504f0-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-212">Data type: **string**</span></span>

<span data-ttu-id="504f0-213">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="504f0-213">Applies to: any</span></span>

<span data-ttu-id="504f0-214">El elemento de tipo de cadena calificado contiene una instancia incrustada.</span><span class="sxs-lookup"><span data-stu-id="504f0-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="504f0-215">El valor de calificador especifica el nombre de una clase CIM en el mismo espacio de nombres que la clase propietaria del elemento calificado.</span><span class="sxs-lookup"><span data-stu-id="504f0-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="504f0-216">La instancia incrustada es una instancia de la clase especificada, incluidas las instancias de sus subclases.</span><span class="sxs-lookup"><span data-stu-id="504f0-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="504f0-217">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gálibo**</span><span class="sxs-lookup"><span data-stu-id="504f0-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-219">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-220">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="504f0-220">Applies to: any</span></span>

<span data-ttu-id="504f0-221">Indica si la propiedad representa un entero no negativo, que puede aumentar o disminuir, pero nunca superar un valor máximo.</span><span class="sxs-lookup"><span data-stu-id="504f0-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="504f0-222">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-222">The default is **FALSE**.</span></span>

<span data-ttu-id="504f0-223">El valor máximo de la propiedad no puede ser mayor que 2 ^*n* -1.</span><span class="sxs-lookup"><span data-stu-id="504f0-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="504f0-224">*N* puede ser 8, 16, 32 o 64, dependiendo del tipo de datos de la propiedad a la que se aplica este calificador.</span><span class="sxs-lookup"><span data-stu-id="504f0-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="504f0-225">El valor de un medidor tiene su valor máximo siempre que la información que se está modelando sea mayor o igual que ese valor máximo.</span><span class="sxs-lookup"><span data-stu-id="504f0-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="504f0-226">Si la información que se modela se reduce posteriormente por debajo del valor máximo, el medidor también se reduce.</span><span class="sxs-lookup"><span data-stu-id="504f0-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="504f0-227">Este calificador solo es aplicable a las propiedades con un tipo de datos entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="504f0-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**De**</span><span class="sxs-lookup"><span data-stu-id="504f0-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-229">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-229">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-230">Se aplica a: parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-230">Applies to: parameters</span></span>

<span data-ttu-id="504f0-231">Indica si el parámetro se utiliza para pasar valores a un método.</span><span class="sxs-lookup"><span data-stu-id="504f0-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="504f0-232">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="504f0-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**</span><span class="sxs-lookup"><span data-stu-id="504f0-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-234">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-234">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-235">Se aplica a: parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-235">Applies to: parameters</span></span>

<span data-ttu-id="504f0-236">Indica si el parámetro es un parámetro de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="504f0-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Clave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="504f0-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="504f0-238">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-238">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-239">Se aplica a: propiedades, referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-239">Applies to: properties, references</span></span>

<span data-ttu-id="504f0-240">Indica si la propiedad forma parte del identificador de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="504f0-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="504f0-241">Si hay más de una propiedad que tiene el calificador de [**clave**](key-qualifier.md) , todas estas propiedades forman colectivamente la clave (una clave compuesta).</span><span class="sxs-lookup"><span data-stu-id="504f0-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="504f0-242">Cuando se toman juntas, las propiedades clave deben proporcionar una referencia única para cada instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="504f0-243">Si este calificador se coloca en una propiedad, solo se permite el valor **true** .</span><span class="sxs-lookup"><span data-stu-id="504f0-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Vago**</span><span class="sxs-lookup"><span data-stu-id="504f0-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-245">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-245">Applies to: properties</span></span>

<span data-ttu-id="504f0-246">Indica que la propiedad utiliza muchos recursos para devolver y requiere mucha memoria y tiempo de procesador.</span><span class="sxs-lookup"><span data-stu-id="504f0-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="504f0-247">WMI mejora el rendimiento de las consultas al no intentar devolver las propiedades marcadas con el calificador **Lazy** .</span><span class="sxs-lookup"><span data-stu-id="504f0-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span><span class="sxs-lookup"><span data-stu-id="504f0-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-249">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-249">Data type: **string array**</span></span>

<span data-ttu-id="504f0-250">Se aplica a: clases, propiedades, asociaciones, indicaciones, referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="504f0-251">Conjunto de valores que indican una ruta de acceso a una ubicación donde puede encontrar más información sobre el origen de una propiedad, clase, Asociación, indicación o referencia.</span><span class="sxs-lookup"><span data-stu-id="504f0-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="504f0-252">La cadena de asignación puede ser una ruta de acceso de directorio, una dirección URL, una clave del registro, un archivo de inclusión, una referencia a una clase CIM o algún otro formato.</span><span class="sxs-lookup"><span data-stu-id="504f0-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="504f0-253">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Máx.**</span><span class="sxs-lookup"><span data-stu-id="504f0-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-255">Tipo de datos: **int**</span><span class="sxs-lookup"><span data-stu-id="504f0-255">Data type: **int**</span></span>

<span data-ttu-id="504f0-256">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-256">Applies to: references</span></span>

<span data-ttu-id="504f0-257">Número máximo de valores que puede tener una referencia determinada para cada conjunto de valores de referencia de la asociación.</span><span class="sxs-lookup"><span data-stu-id="504f0-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="504f0-258">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-258">The default is **NULL**.</span></span> <span data-ttu-id="504f0-259">Por ejemplo, si una asociación relaciona una instancia con instancias B y debe haber como máximo una instancia para cada instancia B, la referencia a debe tener un máximo de un calificador.</span><span class="sxs-lookup"><span data-stu-id="504f0-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="504f0-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-261">Tipo de datos: **int**</span><span class="sxs-lookup"><span data-stu-id="504f0-261">Data type: **int**</span></span>

<span data-ttu-id="504f0-262">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-263">Longitud máxima (en caracteres) de un elemento de datos de **cadena** e indica la compatibilidad con matrices de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="504f0-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="504f0-264">Si se encuentra una matriz de longitud fija, el calificador **MaxLen** contiene la longitud fija encontrada durante el análisis.</span><span class="sxs-lookup"><span data-stu-id="504f0-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="504f0-265">Si se encuentra una matriz de longitud variable, no se utiliza este calificador.</span><span class="sxs-lookup"><span data-stu-id="504f0-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="504f0-266">**MaxLen** se utiliza para sugerir el número máximo de elementos que deben almacenarse en una matriz.</span><span class="sxs-lookup"><span data-stu-id="504f0-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="504f0-267">Al invalidar el valor predeterminado, se puede especificar cualquier valor entero sin signo (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="504f0-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="504f0-268">Un valor **null** (valor predeterminado) implica una longitud ilimitada.</span><span class="sxs-lookup"><span data-stu-id="504f0-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="504f0-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-270">Tipo de datos: **int**</span><span class="sxs-lookup"><span data-stu-id="504f0-270">Data type: **int**</span></span>

<span data-ttu-id="504f0-271">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-272">Valor máximo del objeto.</span><span class="sxs-lookup"><span data-stu-id="504f0-272">Maximum value of the object.</span></span> <span data-ttu-id="504f0-273">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Minuto**</span><span class="sxs-lookup"><span data-stu-id="504f0-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-275">Tipo de datos: **int**</span><span class="sxs-lookup"><span data-stu-id="504f0-275">Data type: **int**</span></span>

<span data-ttu-id="504f0-276">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-276">Applies to: references</span></span>

<span data-ttu-id="504f0-277">Cardinalidad mínima de la referencia (el número mínimo de valores que puede tener una referencia determinada para cada conjunto de valores de referencia de la Asociación).</span><span class="sxs-lookup"><span data-stu-id="504f0-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="504f0-278">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="504f0-278">The default is 0.</span></span>

<span data-ttu-id="504f0-279">Por ejemplo, si una asociación relaciona una instancia con instancias de B y debe haber al menos una instancia de para cada instancia B, la referencia a debe tener como mínimo un calificador.</span><span class="sxs-lookup"><span data-stu-id="504f0-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="504f0-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-281">Tipo de datos: **int**</span><span class="sxs-lookup"><span data-stu-id="504f0-281">Data type: **int**</span></span>

<span data-ttu-id="504f0-282">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-283">Indica el valor mínimo del objeto.</span><span class="sxs-lookup"><span data-stu-id="504f0-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="504f0-284">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span><span class="sxs-lookup"><span data-stu-id="504f0-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-286">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-286">Data type: **string array**</span></span>

<span data-ttu-id="504f0-287">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-287">Applies to: properties</span></span>

<span data-ttu-id="504f0-288">Conjunto de valores que indican la correspondencia entre la propiedad de un objeto y otras propiedades del esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="504f0-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="504f0-289">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-289">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-290">Las propiedades de objeto se identifican con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="504f0-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="504f0-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="504f0-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="504f0-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**No locales**</span><span class="sxs-lookup"><span data-stu-id="504f0-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-293">Data type: **string**</span></span>

<span data-ttu-id="504f0-294">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-294">Applies to: references</span></span>

<span data-ttu-id="504f0-295">Ubicación de una instancia, cuyo valor es <*espacio*>://<*namespacehandle*> el valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="504f0-296">Uso: este calificador no se puede usar con el calificador **NonlocalType** .</span><span class="sxs-lookup"><span data-stu-id="504f0-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span><span class="sxs-lookup"><span data-stu-id="504f0-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-298">Data type: **string**</span></span>

<span data-ttu-id="504f0-299">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-299">Applies to: references</span></span>

<span data-ttu-id="504f0-300">Tipo de ubicación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="504f0-300">Type of location of an instance.</span></span> <span data-ttu-id="504f0-301">Su valor es <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="504f0-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="504f0-302">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-302">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-303">Uso: este calificador no se puede usar con el calificador no **local** .</span><span class="sxs-lookup"><span data-stu-id="504f0-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="504f0-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-305">Data type: **string**</span></span>

<span data-ttu-id="504f0-306">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-306">Applies to: properties</span></span>

<span data-ttu-id="504f0-307">Valor que indica que la propiedad asociada es **null** (la propiedad no tiene un valor válido o significativo).</span><span class="sxs-lookup"><span data-stu-id="504f0-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="504f0-308">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-308">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-309">Las convenciones y restricciones que se usan para definir valores **null** son las mismas que las aplicables al calificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="504f0-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="504f0-310">Nota: este calificador no se puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="504f0-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="504f0-311">No es razonable permitir que una subclase devuelva un valor **null** diferente al de la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="504f0-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Enuncia**</span><span class="sxs-lookup"><span data-stu-id="504f0-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-313">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-313">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-314">Se aplica a: parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-314">Applies to: parameters</span></span>

<span data-ttu-id="504f0-315">Indica si el parámetro devuelve valores de un método.</span><span class="sxs-lookup"><span data-stu-id="504f0-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="504f0-316">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Estima**</span><span class="sxs-lookup"><span data-stu-id="504f0-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-318">Data type: **string**</span></span>

<span data-ttu-id="504f0-319">Se aplica a: propiedades, métodos, referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="504f0-320">Clase primaria o construcción subordinada (propiedad, método o referencia) que es reemplazada por la propiedad, el método o la referencia del mismo nombre en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="504f0-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="504f0-321">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-321">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-322">El formato es:</span><span class="sxs-lookup"><span data-stu-id="504f0-322">The format is:</span></span>

<span data-ttu-id="504f0-323">\[<> de *clase* . \] < *construcción subordinada*></span><span class="sxs-lookup"><span data-stu-id="504f0-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="504f0-324">Si se omite el nombre de clase, la invalidación se aplica a la construcción subordinada en la clase primaria en la jerarquía de clases.</span><span class="sxs-lookup"><span data-stu-id="504f0-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="504f0-325">Uso: el calificador de **invalidación** puede hacer referencia a construcciones basadas solo en el mismo metamodelo.</span><span class="sxs-lookup"><span data-stu-id="504f0-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="504f0-326">No se permite cambiar el nombre o la firma de una construcción durante una operación de invalidación.</span><span class="sxs-lookup"><span data-stu-id="504f0-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span><span class="sxs-lookup"><span data-stu-id="504f0-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-328">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-328">Applies to: classes</span></span>

<span data-ttu-id="504f0-329">Indica si el valor de propiedad en una subclase invalida el valor de una clase primaria.</span><span class="sxs-lookup"><span data-stu-id="504f0-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="504f0-330">La implicación funcional es que, si realiza una consulta en la clase primaria, y si la cláusula **Where** incluye esta propiedad, el elemento primario debe devolver una instancia de con el valor invalidado.</span><span class="sxs-lookup"><span data-stu-id="504f0-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="504f0-331">Como resultado, la administración de Windows ajusta la cláusula **Where** de la consulta enviada a la clase primaria para excluir las referencias a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="504f0-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagan**</span><span class="sxs-lookup"><span data-stu-id="504f0-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-333">Data type: **string**</span></span>

<span data-ttu-id="504f0-334">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-334">Applies to: properties</span></span>

<span data-ttu-id="504f0-335">Nombre de la clave que se va a propagar.</span><span class="sxs-lookup"><span data-stu-id="504f0-335">Name of the key being propagated.</span></span> <span data-ttu-id="504f0-336">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-336">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-337">El uso de este calificador supone la existencia de un solo calificador débil en una referencia que tiene la clase contenedora como su destino.</span><span class="sxs-lookup"><span data-stu-id="504f0-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="504f0-338">La propiedad asociada debe tener el mismo valor que la propiedad denominada por el calificador de la clase en el otro lado de la Asociación débil.</span><span class="sxs-lookup"><span data-stu-id="504f0-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="504f0-339">El formato es:</span><span class="sxs-lookup"><span data-stu-id="504f0-339">The format is:</span></span>

<span data-ttu-id="504f0-340">\[<> de *clase* . \] < *construcción subordinada*></span><span class="sxs-lookup"><span data-stu-id="504f0-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="504f0-341">Uso: cuando se usa el calificador **propagado** , el calificador de [**clave**](key-qualifier.md) debe especificarse con un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="504f0-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lectura**</span><span class="sxs-lookup"><span data-stu-id="504f0-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-343">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-343">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-344">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-344">Applies to: properties</span></span>

<span data-ttu-id="504f0-345">Indica si la propiedad es legible.</span><span class="sxs-lookup"><span data-stu-id="504f0-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="504f0-346">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="504f0-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="504f0-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-348">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-348">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-349">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-349">Applies to: properties</span></span>

<span data-ttu-id="504f0-350">Indica si se requiere un valor distinto de null para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="504f0-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="504f0-351">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisión**</span><span class="sxs-lookup"><span data-stu-id="504f0-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-353">Data type: **string**</span></span>

<span data-ttu-id="504f0-354">Se aplica a: clases, asociaciones, indicaciones, esquemas</span><span class="sxs-lookup"><span data-stu-id="504f0-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="504f0-355">Número de revisión secundaria del objeto de esquema.</span><span class="sxs-lookup"><span data-stu-id="504f0-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="504f0-356">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-356">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-357">Uso: el calificador de **versión** debe estar presente para proporcionar el número de versión principal cuando se use el calificador de **revisión** .</span><span class="sxs-lookup"><span data-stu-id="504f0-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Esquema**</span><span class="sxs-lookup"><span data-stu-id="504f0-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-359">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-359">Data type: **string**</span></span>

<span data-ttu-id="504f0-360">Se aplica a: propiedades, métodos</span><span class="sxs-lookup"><span data-stu-id="504f0-360">Applies to: properties, methods</span></span>

<span data-ttu-id="504f0-361">Nombre del esquema en el que se define la característica.</span><span class="sxs-lookup"><span data-stu-id="504f0-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="504f0-362">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Fuentes**</span><span class="sxs-lookup"><span data-stu-id="504f0-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-364">Data type: **string**</span></span>

<span data-ttu-id="504f0-365">Se aplica a: clases, asociaciones, indicaciones, referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="504f0-366">Ubicación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="504f0-366">Location of an instance.</span></span> <span data-ttu-id="504f0-367">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-367">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-368">El valor del calificador es <*espacio*>://<*namespacehandle*>.</span><span class="sxs-lookup"><span data-stu-id="504f0-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="504f0-369">Uso: el calificador de **origen** no se puede usar con el calificador **sourceType** .</span><span class="sxs-lookup"><span data-stu-id="504f0-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="504f0-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-371">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-371">Data type: **string**</span></span>

<span data-ttu-id="504f0-372">Se aplica a: clases, asociaciones, indicaciones, referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="504f0-373">Tipo de ubicación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="504f0-373">Type of location of an instance.</span></span> <span data-ttu-id="504f0-374">El valor de este calificador es <*espacio*>.</span><span class="sxs-lookup"><span data-stu-id="504f0-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="504f0-375">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-375">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-376">Uso: el calificador **sourceType** no se puede usar con el calificador de **origen** .</span><span class="sxs-lookup"><span data-stu-id="504f0-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="504f0-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-378">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-378">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-379">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-379">Applies to: classes</span></span>

<span data-ttu-id="504f0-380">Indica si la clase admite la creación de instancias de.</span><span class="sxs-lookup"><span data-stu-id="504f0-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="504f0-381">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="504f0-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-383">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-383">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-384">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-384">Applies to: classes</span></span>

<span data-ttu-id="504f0-385">Indica si la clase admite la eliminación de instancias de.</span><span class="sxs-lookup"><span data-stu-id="504f0-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="504f0-386">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span><span class="sxs-lookup"><span data-stu-id="504f0-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-388">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-388">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-389">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-389">Applies to: classes</span></span>

<span data-ttu-id="504f0-390">Indica si la clase admite la modificación (actualización) de instancias de.</span><span class="sxs-lookup"><span data-stu-id="504f0-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="504f0-391">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span><span class="sxs-lookup"><span data-stu-id="504f0-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-393">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-393">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-394">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="504f0-394">Applies to: classes</span></span>

<span data-ttu-id="504f0-395">Indica si la clase puede tener subclases.</span><span class="sxs-lookup"><span data-stu-id="504f0-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="504f0-396">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-396">The default is **FALSE**.</span></span>

<span data-ttu-id="504f0-397">Si se declara una subclase, el compilador genera un error.</span><span class="sxs-lookup"><span data-stu-id="504f0-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="504f0-398">Uso: este calificador no puede coexistir con el calificador **abstracto** .</span><span class="sxs-lookup"><span data-stu-id="504f0-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="504f0-399">Si se especifican los calificadores de **terminal** y **abstractos** , el compilador genera un error.</span><span class="sxs-lookup"><span data-stu-id="504f0-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Participa**</span><span class="sxs-lookup"><span data-stu-id="504f0-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-401">Data type: **string**</span></span>

<span data-ttu-id="504f0-402">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-403">Tipo de unidad en la que se expresa el elemento de datos asociado.</span><span class="sxs-lookup"><span data-stu-id="504f0-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="504f0-404">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-404">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-405">Por ejemplo, un elemento de datos de tamaño podría tener un valor de "bytes" para las **unidades**.</span><span class="sxs-lookup"><span data-stu-id="504f0-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="504f0-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-407">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-407">Data type: **string array**</span></span>

<span data-ttu-id="504f0-408">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-409">Conjunto de valores permitidos para una propiedad, un tipo de valor devuelto de método o un parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="504f0-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="504f0-410">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-410">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-411">Uso: este calificador se puede usar por sí solo o en combinación con el calificador de **valores** .</span><span class="sxs-lookup"><span data-stu-id="504f0-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="504f0-412">Cuando se usa en combinación con el calificador de **valores** , la ubicación del valor en la matriz **ValueMap** proporciona la ubicación de la entrada correspondiente en la matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="504f0-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="504f0-413">Use el calificador **ValueMap** solo con valores de cadena y enteros.</span><span class="sxs-lookup"><span data-stu-id="504f0-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="504f0-414">La sintaxis para representar un valor entero en la matriz de mapa de valores es dígito digit \[ + \| = \] \[ \* \] .</span><span class="sxs-lookup"><span data-stu-id="504f0-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="504f0-415">El contenido, el número máximo de dígitos y el valor representado están restringidos por el tipo de la propiedad asociada.</span><span class="sxs-lookup"><span data-stu-id="504f0-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="504f0-416">Por ejemplo, Uint8 no puede estar firmado, debe tener menos de cuatro dígitos y debe representar un valor inferior a 256.</span><span class="sxs-lookup"><span data-stu-id="504f0-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valor**</span><span class="sxs-lookup"><span data-stu-id="504f0-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-418">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="504f0-418">Data type: **string array**</span></span>

<span data-ttu-id="504f0-419">Se aplica a: propiedades, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="504f0-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="504f0-420">Conjunto de valores que traducen un valor entero en una cadena asociada.</span><span class="sxs-lookup"><span data-stu-id="504f0-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="504f0-421">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-421">The default is **NULL**.</span></span>

<span data-ttu-id="504f0-422">Esta propiedad también especifica una matriz de valores de cadena que se va a asignar a una propiedad de enumeración.</span><span class="sxs-lookup"><span data-stu-id="504f0-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="504f0-423">Este calificador se puede aplicar a una propiedad de entero o a una propiedad de cadena, y la asignación puede ser implícita o explícita.</span><span class="sxs-lookup"><span data-stu-id="504f0-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="504f0-424">Si la asignación es implícita, los valores de propiedad de cadena o entero representan las posiciones ordinales en la matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="504f0-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="504f0-425">Si la asignación es explícita, la propiedad debe ser un entero y los valores de propiedad válidos se muestran en la matriz definida por el calificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="504f0-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="504f0-426">Para obtener más información, consulte [asignación de valores](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="504f0-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="504f0-427">Si no hay ningún calificador **ValueMap** , la matriz **Values** está indizada (relativa a cero) mediante el valor de la propiedad asociada, el tipo de valor devuelto del método o el parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="504f0-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="504f0-428">Si hay un calificador **ValueMap** , el índice de valores se define mediante la ubicación del valor de propiedad en el mapa de valores.</span><span class="sxs-lookup"><span data-stu-id="504f0-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**</span><span class="sxs-lookup"><span data-stu-id="504f0-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="504f0-430">Data type: **string**</span></span>

<span data-ttu-id="504f0-431">Se aplica a: clases, esquemas, asociaciones, indicaciones</span><span class="sxs-lookup"><span data-stu-id="504f0-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="504f0-432">Número de versión principal del objeto de esquema.</span><span class="sxs-lookup"><span data-stu-id="504f0-432">Major version number of the schema object.</span></span> <span data-ttu-id="504f0-433">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="504f0-433">The default is **NULL**.</span></span> <span data-ttu-id="504f0-434">El número de versión se incrementa cuando se realizan cambios en el esquema que modifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="504f0-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Segura**</span><span class="sxs-lookup"><span data-stu-id="504f0-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-436">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-436">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-437">Se aplica a: referencias</span><span class="sxs-lookup"><span data-stu-id="504f0-437">Applies to: references</span></span>

<span data-ttu-id="504f0-438">Indica si las claves de la clase a la que se hace referencia incluyen las claves de los otros participantes de la asociación.</span><span class="sxs-lookup"><span data-stu-id="504f0-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="504f0-439">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-439">The default is **FALSE**.</span></span>

<span data-ttu-id="504f0-440">Este calificador se utiliza cuando la identidad de la clase a la que se hace referencia depende de la identidad de los otros participantes de la asociación.</span><span class="sxs-lookup"><span data-stu-id="504f0-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="504f0-441">No puede haber más de una referencia a una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="504f0-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="504f0-442">Las demás clases de la Asociación deben definir una clave.</span><span class="sxs-lookup"><span data-stu-id="504f0-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="504f0-443">Las claves de las otras clases de la asociación se repiten en la clase a la que se hace referencia y se etiquetan con un calificador **propagado** .</span><span class="sxs-lookup"><span data-stu-id="504f0-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Escribi**</span><span class="sxs-lookup"><span data-stu-id="504f0-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-445">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-445">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-446">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-446">Applies to: properties</span></span>

<span data-ttu-id="504f0-447">Indica que las aplicaciones o los scripts pueden cambiar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="504f0-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="504f0-448">La cuenta que ejecuta la aplicación debe tener acceso al espacio de nombres que contiene las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="504f0-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="504f0-449">La implementación del proveedor también puede limitar el acceso a los datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="504f0-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="504f0-450">Un valor de **true** indica que la propiedad es legible y grabable por los consumidores a los que se les permite el acceso mediante WMI y el proveedor.</span><span class="sxs-lookup"><span data-stu-id="504f0-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="504f0-451">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-451">The default is **FALSE**.</span></span>

<span data-ttu-id="504f0-452">Todavía es posible escribir en una propiedad que no tenga el calificador de **escritura** .</span><span class="sxs-lookup"><span data-stu-id="504f0-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="504f0-453">La implementación del proveedor puede permitir que se modifiquen las propiedades de las clases del proveedor, tanto si el calificador de **escritura** está presente.</span><span class="sxs-lookup"><span data-stu-id="504f0-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span><span class="sxs-lookup"><span data-stu-id="504f0-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-455">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-455">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-456">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-456">Applies to: properties</span></span>

<span data-ttu-id="504f0-457">Indica si la propiedad es grabable en la creación de la instancia.</span><span class="sxs-lookup"><span data-stu-id="504f0-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="504f0-458">Este calificador se puede usar junto con el calificador **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="504f0-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="504f0-459">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="504f0-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span><span class="sxs-lookup"><span data-stu-id="504f0-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="504f0-461">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="504f0-461">Data type: **boolean**</span></span>

<span data-ttu-id="504f0-462">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="504f0-462">Applies to: properties</span></span>

<span data-ttu-id="504f0-463">Indica si la propiedad es grabable en la actualización de la instancia.</span><span class="sxs-lookup"><span data-stu-id="504f0-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="504f0-464">Este calificador se puede usar junto con el calificador **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="504f0-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="504f0-465">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="504f0-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="504f0-466">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="504f0-466">Examples</span></span>

<span data-ttu-id="504f0-467">Para obtener más información sobre cómo recuperar calificadores, vea el ejemplo de código de PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) en la galería de TechNet.</span><span class="sxs-lookup"><span data-stu-id="504f0-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="504f0-468">Requisitos</span><span class="sxs-lookup"><span data-stu-id="504f0-468">Requirements</span></span>



| <span data-ttu-id="504f0-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="504f0-469">Requirement</span></span> | <span data-ttu-id="504f0-470">Value</span><span class="sxs-lookup"><span data-stu-id="504f0-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="504f0-471">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="504f0-471">Minimum supported client</span></span><br/> | <span data-ttu-id="504f0-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="504f0-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="504f0-473">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="504f0-473">Minimum supported server</span></span><br/> | <span data-ttu-id="504f0-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="504f0-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="504f0-475">Vea también</span><span class="sxs-lookup"><span data-stu-id="504f0-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504f0-476">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="504f0-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="504f0-477">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="504f0-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




