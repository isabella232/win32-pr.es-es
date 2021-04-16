---
title: Elemento HelpButton
description: Representa el control de botón de ayuda.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- HelpButton cinta de opciones de Windows
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105695522"
---
# <a name="helpbutton-element"></a><span data-ttu-id="2db20-104">Elemento HelpButton</span><span class="sxs-lookup"><span data-stu-id="2db20-104">HelpButton element</span></span>

<span data-ttu-id="2db20-105">Representa el control de [botón de ayuda](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="2db20-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2db20-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2db20-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="2db20-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2db20-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2db20-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2db20-108">Attribute</span></span></th>
<th><span data-ttu-id="2db20-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2db20-109">Type</span></span></th>
<th><span data-ttu-id="2db20-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2db20-110">Required</span></span></th>
<th><span data-ttu-id="2db20-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db20-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2db20-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2db20-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2db20-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="2db20-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2db20-114">No</span><span class="sxs-lookup"><span data-stu-id="2db20-114">No</span></span><br/></td>
<td><span data-ttu-id="2db20-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2db20-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2db20-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="2db20-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2db20-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2db20-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2db20-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2db20-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2db20-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2db20-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2db20-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2db20-120">Child elements</span></span>

<span data-ttu-id="2db20-121">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="2db20-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2db20-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2db20-122">Parent elements</span></span>



| <span data-ttu-id="2db20-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="2db20-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="2db20-124">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="2db20-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2db20-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2db20-125">Remarks</span></span>

<span data-ttu-id="2db20-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2db20-126">Optional.</span></span>

<span data-ttu-id="2db20-127">Puede producirse una vez como máximo para cada cinta de opciones [**. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="2db20-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="2db20-128">Inicia un cuadro de diálogo de ayuda de la aplicación al hacer clic en él.</span><span class="sxs-lookup"><span data-stu-id="2db20-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="2db20-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2db20-129">Examples</span></span>

<span data-ttu-id="2db20-130">En el ejemplo siguiente se muestra el marcado básico necesario para implementar un control de [botón de ayuda](windowsribbon-controls-helpbutton.md) de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2db20-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="2db20-131">En esta sección de código se muestra la declaración del comando **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="2db20-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="2db20-132">En esta sección de código se muestra la declaración de control **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="2db20-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="2db20-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2db20-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2db20-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2db20-134">Minimum supported system</span></span><br/> | <span data-ttu-id="2db20-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2db20-135">Windows 7</span></span> |
| <span data-ttu-id="2db20-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2db20-136">Can be empty</span></span>                        | <span data-ttu-id="2db20-137">Sí</span><span class="sxs-lookup"><span data-stu-id="2db20-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="2db20-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2db20-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db20-139">Control de botón de ayuda</span><span class="sxs-lookup"><span data-stu-id="2db20-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





