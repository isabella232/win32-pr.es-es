---
description: Describe un espacio de nombres.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380849"
---
# <a name="namespace-element"></a><span data-ttu-id="62fe2-103">nameSpace, elemento</span><span class="sxs-lookup"><span data-stu-id="62fe2-103">nameSpace element</span></span>

<span data-ttu-id="62fe2-104">Describe un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="62fe2-104">Describes a namespace.</span></span> <span data-ttu-id="62fe2-105">Este espacio de nombres se puede usar para la generación de código o para las \<wsdl:import> directivas de control.</span><span class="sxs-lookup"><span data-stu-id="62fe2-105">This namespace may be used for code generation or for handling \<wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="62fe2-106">Uso</span><span class="sxs-lookup"><span data-stu-id="62fe2-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="62fe2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="62fe2-107">Attributes</span></span>



| <span data-ttu-id="62fe2-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="62fe2-108">Attribute</span></span>          | <span data-ttu-id="62fe2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="62fe2-109">Type</span></span>                         | <span data-ttu-id="62fe2-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="62fe2-110">Required</span></span>       | <span data-ttu-id="62fe2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="62fe2-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="62fe2-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="62fe2-112">**uri**</span></span><br/> | <span data-ttu-id="62fe2-113">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="62fe2-113">character\_string</span></span><br/> | <span data-ttu-id="62fe2-114">Sí</span><span class="sxs-lookup"><span data-stu-id="62fe2-114">Yes</span></span><br/> | <span data-ttu-id="62fe2-115">URI único del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="62fe2-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="62fe2-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62fe2-116">Child elements</span></span>



| <span data-ttu-id="62fe2-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="62fe2-117">Element</span></span>                                               | <span data-ttu-id="62fe2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="62fe2-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62fe2-119">**Codename**</span><span class="sxs-lookup"><span data-stu-id="62fe2-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="62fe2-120">Nombre que se va a usar para identificar el espacio de nombres en el código generado.</span><span class="sxs-lookup"><span data-stu-id="62fe2-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="62fe2-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="62fe2-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="62fe2-122">Prefijo que se va a usar en el código generado para los nombres de macros en el espacio de nombres .</span><span class="sxs-lookup"><span data-stu-id="62fe2-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="62fe2-123">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="62fe2-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="62fe2-124">Nombre completo en el espacio de nombres .</span><span class="sxs-lookup"><span data-stu-id="62fe2-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="62fe2-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="62fe2-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="62fe2-126">Prefijo al que se debe asignar el espacio de nombres para que el XML sea más legible.</span><span class="sxs-lookup"><span data-stu-id="62fe2-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="62fe2-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62fe2-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="62fe2-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="62fe2-128">Parent elements</span></span>



| <span data-ttu-id="62fe2-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="62fe2-129">Element</span></span>                                     | <span data-ttu-id="62fe2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="62fe2-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="62fe2-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="62fe2-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="62fe2-132">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="62fe2-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="62fe2-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62fe2-133">Remarks</span></span>

<span data-ttu-id="62fe2-134">Este elemento se puede usar para proporcionar al generador de código información adicional sobre los espacios de nombres que encuentra en los archivos WSDL y XSD o para introducir nuevos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="62fe2-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="62fe2-135">Los espacios de nombres implícitos en la reflexión de tipos o especificados en los archivos WSDL y XSD se analizan automáticamente por el generador de código y no tienen que definirse explícitamente en el script.</span><span class="sxs-lookup"><span data-stu-id="62fe2-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="62fe2-136">En algunos casos, este elemento se puede usar para agregar propiedades o nombres adicionales a un espacio de nombres al que hace referencia la reflexión de tipos o WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="62fe2-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="62fe2-137">El generador de código no lo considera un conflicto.</span><span class="sxs-lookup"><span data-stu-id="62fe2-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="62fe2-138">El xml siguiente muestra un elemento nameSpace (con elementos secundarios omitidos por brevedad).</span><span class="sxs-lookup"><span data-stu-id="62fe2-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="62fe2-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="62fe2-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="62fe2-140">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62fe2-140">Minimum supported system</span></span><br/> | <span data-ttu-id="62fe2-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62fe2-141">Windows Vista</span></span> |
| <span data-ttu-id="62fe2-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="62fe2-142">Can be empty</span></span>                        | <span data-ttu-id="62fe2-143">Sí</span><span class="sxs-lookup"><span data-stu-id="62fe2-143">Yes</span></span>           |



 

 




