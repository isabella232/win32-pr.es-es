---
description: Incluye el contenido de una macro o un archivo en la salida generada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include [elemento]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995782"
---
# <a name="include-element"></a><span data-ttu-id="b1761-103">include [elemento]</span><span class="sxs-lookup"><span data-stu-id="b1761-103">include element</span></span>

<span data-ttu-id="b1761-104">Incluye el contenido de una macro o un archivo en la salida generada.</span><span class="sxs-lookup"><span data-stu-id="b1761-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="b1761-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b1761-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="b1761-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1761-106">Attributes</span></span>



| <span data-ttu-id="b1761-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b1761-107">Attribute</span></span>            | <span data-ttu-id="b1761-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1761-108">Type</span></span>                         | <span data-ttu-id="b1761-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b1761-109">Required</span></span>      | <span data-ttu-id="b1761-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1761-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="b1761-111">**file**</span><span class="sxs-lookup"><span data-stu-id="b1761-111">**file**</span></span><br/>  | <span data-ttu-id="b1761-112">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="b1761-112">character\_string</span></span><br/> | <span data-ttu-id="b1761-113">No</span><span class="sxs-lookup"><span data-stu-id="b1761-113">No</span></span><br/> | <span data-ttu-id="b1761-114">Ruta de acceso al archivo que se incluirá.</span><span class="sxs-lookup"><span data-stu-id="b1761-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="b1761-115">**Macro**</span><span class="sxs-lookup"><span data-stu-id="b1761-115">**macro**</span></span><br/> | <span data-ttu-id="b1761-116">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="b1761-116">character\_string</span></span><br/> | <span data-ttu-id="b1761-117">No</span><span class="sxs-lookup"><span data-stu-id="b1761-117">No</span></span><br/> | <span data-ttu-id="b1761-118">Nombre de la macro que se incluirá.</span><span class="sxs-lookup"><span data-stu-id="b1761-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b1761-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1761-119">Child elements</span></span>

<span data-ttu-id="b1761-120">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b1761-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b1761-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b1761-121">Parent elements</span></span>



| <span data-ttu-id="b1761-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1761-122">Element</span></span>                         | <span data-ttu-id="b1761-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1761-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1761-124">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b1761-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b1761-125">Indica al generador de código que genere un archivo y especifica el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="b1761-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b1761-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1761-126">Remarks</span></span>

<span data-ttu-id="b1761-127">Se debe **especificar el** **atributo** de macro o el atributo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b1761-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="b1761-128">No especifique ambos atributos.</span><span class="sxs-lookup"><span data-stu-id="b1761-128">Do not specify both attributes.</span></span>

<span data-ttu-id="b1761-129">WsdCodeGen define una macro denominada **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="b1761-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="b1761-130">Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.</span><span class="sxs-lookup"><span data-stu-id="b1761-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="b1761-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b1761-131">Examples</span></span>

<span data-ttu-id="b1761-132">En el xml siguiente se muestra cómo incluir la macro **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="b1761-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="b1761-133">Este XML se puede agregar a un archivo de configuración XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="b1761-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="b1761-134">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b1761-134">Element information</span></span>



| <span data-ttu-id="b1761-135">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b1761-135">Label</span></span> | <span data-ttu-id="b1761-136">Value</span><span class="sxs-lookup"><span data-stu-id="b1761-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b1761-137">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1761-137">Minimum supported system</span></span><br/> | <span data-ttu-id="b1761-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1761-138">Windows Vista</span></span> |
| <span data-ttu-id="b1761-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1761-139">Can be empty</span></span>                        | <span data-ttu-id="b1761-140">Sí</span><span class="sxs-lookup"><span data-stu-id="b1761-140">Yes</span></span>           |



 

 




