---
description: Describe un espacio de nombres.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: Espacio de nombres (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544798"
---
# <a name="namespace-element"></a><span data-ttu-id="98627-103">Espacio de nombres (elemento)</span><span class="sxs-lookup"><span data-stu-id="98627-103">nameSpace element</span></span>

<span data-ttu-id="98627-104">Describe un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98627-104">Describes a namespace.</span></span> <span data-ttu-id="98627-105">Este espacio de nombres se puede usar para la generación de código o para controlar <las directivas WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="98627-105">This namespace may be used for code generation or for handling <wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="98627-106">Uso</span><span class="sxs-lookup"><span data-stu-id="98627-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="98627-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="98627-107">Attributes</span></span>



| <span data-ttu-id="98627-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="98627-108">Attribute</span></span>          | <span data-ttu-id="98627-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="98627-109">Type</span></span>                         | <span data-ttu-id="98627-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="98627-110">Required</span></span>       | <span data-ttu-id="98627-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="98627-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="98627-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="98627-112">**uri**</span></span><br/> | <span data-ttu-id="98627-113">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="98627-113">character\_string</span></span><br/> | <span data-ttu-id="98627-114">Sí</span><span class="sxs-lookup"><span data-stu-id="98627-114">Yes</span></span><br/> | <span data-ttu-id="98627-115">Identificador URI único del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98627-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="98627-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98627-116">Child elements</span></span>



| <span data-ttu-id="98627-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="98627-117">Element</span></span>                                               | <span data-ttu-id="98627-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="98627-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98627-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="98627-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="98627-120">Nombre que se va a usar para identificar el espacio de nombres en el código generado.</span><span class="sxs-lookup"><span data-stu-id="98627-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="98627-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="98627-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="98627-122">El prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98627-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="98627-123">**name**</span><span class="sxs-lookup"><span data-stu-id="98627-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="98627-124">Nombre completo en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98627-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="98627-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="98627-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="98627-126">El prefijo al que se debe asignar el espacio de nombres para que el código XML sea más legible.</span><span class="sxs-lookup"><span data-stu-id="98627-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="98627-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98627-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="98627-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="98627-128">Parent elements</span></span>



| <span data-ttu-id="98627-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="98627-129">Element</span></span>                                     | <span data-ttu-id="98627-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="98627-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="98627-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="98627-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="98627-132">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="98627-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="98627-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98627-133">Remarks</span></span>

<span data-ttu-id="98627-134">Este elemento se puede usar para proporcionar al generador de código información adicional sobre los espacios de nombres que encuentra en los archivos WSDL y XSD, o para introducir nuevos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="98627-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="98627-135">El generador de código analiza automáticamente los espacios de nombres implícitos en la reflexión de tipos o que se especifican en archivos WSDL y XSD y no es necesario que se definan explícitamente en el script.</span><span class="sxs-lookup"><span data-stu-id="98627-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="98627-136">En algunos casos, este elemento se puede usar para agregar propiedades o nombres adicionales a un espacio de nombres al que se hace referencia mediante reflexión de tipos o WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="98627-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="98627-137">El generador de código no tiene en cuenta esto como un conflicto.</span><span class="sxs-lookup"><span data-stu-id="98627-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="98627-138">En el código XML siguiente se muestra un elemento nameSpace (con elementos secundarios omitidos por motivos de brevedad).</span><span class="sxs-lookup"><span data-stu-id="98627-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="98627-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="98627-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="98627-140">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98627-140">Minimum supported system</span></span><br/> | <span data-ttu-id="98627-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98627-141">Windows Vista</span></span> |
| <span data-ttu-id="98627-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98627-142">Can be empty</span></span>                        | <span data-ttu-id="98627-143">Sí</span><span class="sxs-lookup"><span data-stu-id="98627-143">Yes</span></span>           |



 

 




