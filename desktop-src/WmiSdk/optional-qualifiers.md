---
description: Los calificadores opcionales abordan situaciones recurrentes que no son comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Calificadores opcionales
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707209"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="22c94-103">Calificadores opcionales</span><span class="sxs-lookup"><span data-stu-id="22c94-103">Optional Qualifiers</span></span>

<span data-ttu-id="22c94-104">Los calificadores opcionales abordan situaciones recurrentes que no son comunes a todas las implementaciones compatibles con CIM, que no son necesarias para interpretar estos calificadores.</span><span class="sxs-lookup"><span data-stu-id="22c94-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="22c94-105">Se proporcionan calificadores opcionales en la especificación para evitar calificadores definidos por el usuario aleatorios que puedan producirse en estas situaciones recurrentes.</span><span class="sxs-lookup"><span data-stu-id="22c94-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="22c94-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="22c94-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-107">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-107">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-108">Se aplica a: asociaciones, referencias</span><span class="sxs-lookup"><span data-stu-id="22c94-108">Applies to: associations, references</span></span>

<span data-ttu-id="22c94-109">En el caso de las asociaciones, indica si se debe eliminar la Asociación calificada si se elimina cualquiera de los objetos a los que se hace referencia en la asociación y si el objeto correspondiente al que se hace referencia en la asociación está calificado con **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="22c94-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="22c94-110">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-110">The default is **FALSE**.</span></span>

<span data-ttu-id="22c94-111">En el caso de las referencias, este calificador indica si el objeto al que se hace referencia debe eliminarse si la asociación que contiene la referencia se elimina y se califica con **IfDeleted**, o si se elimina cualquiera de los objetos a los que se hace referencia en la asociación y el objeto al que se hace referencia en la asociación está calificado con **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="22c94-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="22c94-112">Uso: las aplicaciones deben realizar un seguimiento de las asociaciones y las referencias marcadas con el calificador de **eliminación** y eliminar la asociación o la referencia de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="22c94-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="22c94-113">Si se ha eliminado un objeto de la asociación, pero no está marcado con **IfDeleted**, no se debe eliminar la asociación.</span><span class="sxs-lookup"><span data-stu-id="22c94-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="22c94-114">Esta regla de uso debe comprobarse cuando se define el modelo de seguridad de CIM.</span><span class="sxs-lookup"><span data-stu-id="22c94-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Alto**</span><span class="sxs-lookup"><span data-stu-id="22c94-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-116">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-117">Se aplica a: propiedades, referencias, clases, asociaciones, métodos</span><span class="sxs-lookup"><span data-stu-id="22c94-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="22c94-118">Indica si la acción implícita requiere un cálculo extensivo.</span><span class="sxs-lookup"><span data-stu-id="22c94-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="22c94-119">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span><span class="sxs-lookup"><span data-stu-id="22c94-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-121">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-122">Se aplica a: asociaciones y referencias</span><span class="sxs-lookup"><span data-stu-id="22c94-122">Applies to: associations and references</span></span>

<span data-ttu-id="22c94-123">Indica si se deben eliminar todos los objetos dentro de una asociación que califique por **Delete** si se elimina el objeto al que se hace referencia o la asociación.</span><span class="sxs-lookup"><span data-stu-id="22c94-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="22c94-124">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indizó**</span><span class="sxs-lookup"><span data-stu-id="22c94-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-126">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-127">Se aplica a: propiedades, métodos</span><span class="sxs-lookup"><span data-stu-id="22c94-127">Applies to: properties, methods</span></span>

<span data-ttu-id="22c94-128">Indica si se debe indizar una propiedad de clase.</span><span class="sxs-lookup"><span data-stu-id="22c94-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="22c94-129">Cuando se aplica a las propiedades de las clases hospedadas por el repositorio, solo tiene el significado de crear (en el momento de crear la clase) una búsqueda rápida de consultas secundarias para esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="22c94-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="22c94-130">Solo se permite el valor **true** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="22c94-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Ve**</span><span class="sxs-lookup"><span data-stu-id="22c94-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-132">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-133">Se aplica a: asociaciones, propiedades, métodos, referencias, clases</span><span class="sxs-lookup"><span data-stu-id="22c94-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="22c94-134">Indica si la asociación se define solo para fines internos (por ejemplo, para la definición de la semántica de dependencia) y no debe mostrarse (por ejemplo, en Maps).</span><span class="sxs-lookup"><span data-stu-id="22c94-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="22c94-135">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Amplíe**</span><span class="sxs-lookup"><span data-stu-id="22c94-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-137">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-138">Se aplica a: propiedades, clases</span><span class="sxs-lookup"><span data-stu-id="22c94-138">Applies to: properties, classes</span></span>

<span data-ttu-id="22c94-139">Indica si la propiedad o la clase requieren una gran cantidad de espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="22c94-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="22c94-140">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**No \_ null**</span><span class="sxs-lookup"><span data-stu-id="22c94-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-142">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-143">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="22c94-143">Applies to: properties</span></span>

<span data-ttu-id="22c94-144">Indica si una propiedad de clase no puede tomar un valor **null** (**VT \_ null**).</span><span class="sxs-lookup"><span data-stu-id="22c94-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="22c94-145">Solo se permite el valor **true** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="22c94-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="22c94-146">Si se especifica este calificador, WMI no permite la creación de instancias con la propiedad establecida en **null** y las propiedades **null** devuelven el código de error **null de WBEM \_ e \_ no válido \_** .</span><span class="sxs-lookup"><span data-stu-id="22c94-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="22c94-147">Tenga en cuenta que la [**clave**](standard-qualifiers.md) y los calificadores **indizados** ya implican este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="22c94-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Presta**</span><span class="sxs-lookup"><span data-stu-id="22c94-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22c94-149">Data type: **string**</span></span>

<span data-ttu-id="22c94-150">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="22c94-150">Applies to: Any</span></span>

<span data-ttu-id="22c94-151">Indica que el elemento de esquema es dinámico y, por tanto, lo rellena un proveedor.</span><span class="sxs-lookup"><span data-stu-id="22c94-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="22c94-152">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-152">The default is **NULL**.</span></span> <span data-ttu-id="22c94-153">Este calificador es un identificador específico de la implementación para la instrumentación.</span><span class="sxs-lookup"><span data-stu-id="22c94-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Ensayo**</span><span class="sxs-lookup"><span data-stu-id="22c94-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-155">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22c94-155">Data type: **boolean**</span></span>

<span data-ttu-id="22c94-156">Se aplica a: any</span><span class="sxs-lookup"><span data-stu-id="22c94-156">Applies to: any</span></span>

<span data-ttu-id="22c94-157">Indica que se ha propuesto que el elemento especificado forme parte de una versión futura de los esquemas CIM, pero que aún no forma parte del esquema estándar.</span><span class="sxs-lookup"><span data-stu-id="22c94-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="22c94-158">En su lugar, el elemento está disponible para que los usuarios experimenten, implementen y proporcionen comentarios sobre.</span><span class="sxs-lookup"><span data-stu-id="22c94-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="22c94-159">En función de los comentarios, el elemento se puede Agregar al estándar como se presenta, se modifica o se quita.</span><span class="sxs-lookup"><span data-stu-id="22c94-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="22c94-160">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="22c94-160">The default is **FALSE**.</span></span> <span data-ttu-id="22c94-161">Una implementación de no tiene que admitir un elemento con este calificador.</span><span class="sxs-lookup"><span data-stu-id="22c94-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="22c94-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22c94-163">Data type: **string**</span></span>

<span data-ttu-id="22c94-164">Se aplica a: propiedades, referencias, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="22c94-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="22c94-165">Tipo específico asignado a un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="22c94-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="22c94-166">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-166">The default is **NULL**.</span></span>

<span data-ttu-id="22c94-167">Uso: debe usar el calificador **SyntaxType** con este calificador.</span><span class="sxs-lookup"><span data-stu-id="22c94-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span><span class="sxs-lookup"><span data-stu-id="22c94-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22c94-169">Data type: **string**</span></span>

<span data-ttu-id="22c94-170">Se aplica a: propiedades, referencias, métodos, parámetros</span><span class="sxs-lookup"><span data-stu-id="22c94-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="22c94-171">Formato del calificador de **Sintaxis** .</span><span class="sxs-lookup"><span data-stu-id="22c94-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="22c94-172">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-172">The default is **NULL**.</span></span>

<span data-ttu-id="22c94-173">Uso: debe utilizar el calificador de **Sintaxis** con este calificador.</span><span class="sxs-lookup"><span data-stu-id="22c94-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="22c94-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22c94-175">Data type: **string**</span></span>

<span data-ttu-id="22c94-176">Se aplica a: clases, propiedades, métodos, asociaciones, indicaciones, referencias</span><span class="sxs-lookup"><span data-stu-id="22c94-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="22c94-177">Circunstancias en las que se activa un desencadenador.</span><span class="sxs-lookup"><span data-stu-id="22c94-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="22c94-178">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-178">The default is **NULL**.</span></span> <span data-ttu-id="22c94-179">Los tipos de desencadenador varían según la construcción de metamodelo.</span><span class="sxs-lookup"><span data-stu-id="22c94-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="22c94-180">En el caso de las clases y asociaciones, los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="22c94-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="22c94-181">Crear</span><span class="sxs-lookup"><span data-stu-id="22c94-181">Create</span></span>

<span data-ttu-id="22c94-182">Eliminar</span><span class="sxs-lookup"><span data-stu-id="22c94-182">Delete</span></span>

<span data-ttu-id="22c94-183">Actualizar</span><span class="sxs-lookup"><span data-stu-id="22c94-183">Update</span></span>

<span data-ttu-id="22c94-184">Access</span><span class="sxs-lookup"><span data-stu-id="22c94-184">Access</span></span>

<span data-ttu-id="22c94-185">En el caso de las propiedades y referencias, los valores válidos son: Update y Access.</span><span class="sxs-lookup"><span data-stu-id="22c94-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="22c94-186">En el caso de los métodos, los valores válidos son Before y after.</span><span class="sxs-lookup"><span data-stu-id="22c94-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="22c94-187">En el caso de las indicaciones, se produce el valor legal.</span><span class="sxs-lookup"><span data-stu-id="22c94-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span><span class="sxs-lookup"><span data-stu-id="22c94-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-189">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="22c94-189">Data type: **string array**</span></span>

<span data-ttu-id="22c94-190">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="22c94-190">Applies to: properties</span></span>

<span data-ttu-id="22c94-191">Conjunto de valores que indican que el valor de la propiedad asociada es desconocido (la propiedad no se puede considerar como si tuviera un valor válido o significativo).</span><span class="sxs-lookup"><span data-stu-id="22c94-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="22c94-192">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-192">The default is **NULL**.</span></span>

<span data-ttu-id="22c94-193">Las convenciones y restricciones que se usan para definir valores desconocidos son las mismas que las aplicables al calificador [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="22c94-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="22c94-194">Tenga en cuenta que este calificador no se puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="22c94-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="22c94-195">No es razonable permitir que una subclase trate un valor como un valor conocido cuando alguna clase primaria lo trata como desconocido.</span><span class="sxs-lookup"><span data-stu-id="22c94-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="22c94-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span><span class="sxs-lookup"><span data-stu-id="22c94-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="22c94-197">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="22c94-197">Data type: **string array**</span></span>

<span data-ttu-id="22c94-198">Se aplica a: propiedades</span><span class="sxs-lookup"><span data-stu-id="22c94-198">Applies to: properties</span></span>

<span data-ttu-id="22c94-199">Conjunto de valores que indican que el valor de la propiedad asociada no se admite (la propiedad no se puede considerar como si tuviera un valor válido o significativo).</span><span class="sxs-lookup"><span data-stu-id="22c94-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="22c94-200">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="22c94-200">The default is **NULL**.</span></span>

<span data-ttu-id="22c94-201">Las convenciones y restricciones que se usan para definir valores no admitidos son las mismas que las aplicables al calificador [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="22c94-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="22c94-202">Nota: este calificador no se puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="22c94-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="22c94-203">No es razonable permitir que una subclase trate un valor como un valor admitido que alguna clase primaria trata como desconocido.</span><span class="sxs-lookup"><span data-stu-id="22c94-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22c94-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c94-204">Requirements</span></span>



| <span data-ttu-id="22c94-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c94-205">Requirement</span></span> | <span data-ttu-id="22c94-206">Value</span><span class="sxs-lookup"><span data-stu-id="22c94-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="22c94-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22c94-207">Minimum supported client</span></span><br/> | <span data-ttu-id="22c94-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c94-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="22c94-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22c94-209">Minimum supported server</span></span><br/> | <span data-ttu-id="22c94-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22c94-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22c94-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="22c94-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c94-212">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="22c94-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="22c94-213">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="22c94-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




