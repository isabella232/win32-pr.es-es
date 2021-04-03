---
description: Incluye el contenido de una macro o un archivo en la salida generada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include [elemento]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083069"
---
# <a name="include-element"></a><span data-ttu-id="33230-103">include [elemento]</span><span class="sxs-lookup"><span data-stu-id="33230-103">include element</span></span>

<span data-ttu-id="33230-104">Incluye el contenido de una macro o un archivo en la salida generada.</span><span class="sxs-lookup"><span data-stu-id="33230-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="33230-105">Uso</span><span class="sxs-lookup"><span data-stu-id="33230-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="33230-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="33230-106">Attributes</span></span>



| <span data-ttu-id="33230-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="33230-107">Attribute</span></span>            | <span data-ttu-id="33230-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="33230-108">Type</span></span>                         | <span data-ttu-id="33230-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="33230-109">Required</span></span>      | <span data-ttu-id="33230-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="33230-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="33230-111">**file**</span><span class="sxs-lookup"><span data-stu-id="33230-111">**file**</span></span><br/>  | <span data-ttu-id="33230-112">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="33230-112">character\_string</span></span><br/> | <span data-ttu-id="33230-113">No</span><span class="sxs-lookup"><span data-stu-id="33230-113">No</span></span><br/> | <span data-ttu-id="33230-114">Ruta de acceso al archivo que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="33230-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="33230-115">**macro**</span><span class="sxs-lookup"><span data-stu-id="33230-115">**macro**</span></span><br/> | <span data-ttu-id="33230-116">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="33230-116">character\_string</span></span><br/> | <span data-ttu-id="33230-117">No</span><span class="sxs-lookup"><span data-stu-id="33230-117">No</span></span><br/> | <span data-ttu-id="33230-118">Nombre de la macro que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="33230-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="33230-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33230-119">Child elements</span></span>

<span data-ttu-id="33230-120">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="33230-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="33230-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="33230-121">Parent elements</span></span>



| <span data-ttu-id="33230-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="33230-122">Element</span></span>                         | <span data-ttu-id="33230-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="33230-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33230-124">**archivo**</span><span class="sxs-lookup"><span data-stu-id="33230-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="33230-125">Dirige el generador de código para generar un archivo y especifica el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="33230-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="33230-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33230-126">Remarks</span></span>

<span data-ttu-id="33230-127">Se debe especificar el atributo de **macro** o el atributo de **archivo** .</span><span class="sxs-lookup"><span data-stu-id="33230-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="33230-128">No especifique ninguno de los dos atributos.</span><span class="sxs-lookup"><span data-stu-id="33230-128">Do not specify both attributes.</span></span>

<span data-ttu-id="33230-129">WsdCodeGen define una macro denominada **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="33230-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="33230-130">Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.</span><span class="sxs-lookup"><span data-stu-id="33230-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="33230-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="33230-131">Examples</span></span>

<span data-ttu-id="33230-132">El siguiente XML muestra cómo incluir la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="33230-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="33230-133">Este XML se puede Agregar a un archivo de configuración XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="33230-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="33230-134">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="33230-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="33230-135">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33230-135">Minimum supported system</span></span><br/> | <span data-ttu-id="33230-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33230-136">Windows Vista</span></span> |
| <span data-ttu-id="33230-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="33230-137">Can be empty</span></span>                        | <span data-ttu-id="33230-138">Sí</span><span class="sxs-lookup"><span data-stu-id="33230-138">Yes</span></span>           |



 

 




