---
title: Elemento QuickAccessToolbar
description: Representa la barra de herramientas de acceso rápido (QAT), una pequeña barra de herramientas que muestra accesos directos a comandos de la cinta de opciones.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- QuickAccessToolbar cinta de opciones de Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420197"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="37d26-104">Elemento QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="37d26-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="37d26-105">Representa la [barra de herramientas de acceso rápido (Qat)](windowsribbon-controls-quickaccesstoolbar.md), una pequeña barra de herramientas que muestra accesos directos a comandos de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="37d26-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="37d26-106">Uso</span><span class="sxs-lookup"><span data-stu-id="37d26-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="37d26-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="37d26-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37d26-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="37d26-108">Attribute</span></span></th>
<th><span data-ttu-id="37d26-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="37d26-109">Type</span></span></th>
<th><span data-ttu-id="37d26-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="37d26-110">Required</span></span></th>
<th><span data-ttu-id="37d26-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37d26-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37d26-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="37d26-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="37d26-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="37d26-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="37d26-114">No</span><span class="sxs-lookup"><span data-stu-id="37d26-114">No</span></span><br/></td>
<td><span data-ttu-id="37d26-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37d26-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="37d26-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="37d26-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="37d26-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="37d26-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="37d26-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="37d26-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="37d26-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="37d26-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37d26-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="37d26-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="37d26-121">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="37d26-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="37d26-122">No</span><span class="sxs-lookup"><span data-stu-id="37d26-122">No</span></span><br/></td>
<td><span data-ttu-id="37d26-123">Inserta un elemento de comando adicional en el menú QAT.</span><span class="sxs-lookup"><span data-stu-id="37d26-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="37d26-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="37d26-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="37d26-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="37d26-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="37d26-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="37d26-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="37d26-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="37d26-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="37d26-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37d26-128">Child elements</span></span>



| <span data-ttu-id="37d26-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="37d26-129">Element</span></span>                                                                                                                   | <span data-ttu-id="37d26-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="37d26-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="37d26-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="37d26-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="37d26-132">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="37d26-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="37d26-133">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="37d26-133">Parent elements</span></span>



| <span data-ttu-id="37d26-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="37d26-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37d26-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="37d26-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="37d26-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37d26-136">Remarks</span></span>

<span data-ttu-id="37d26-137">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37d26-137">Required.</span></span>

<span data-ttu-id="37d26-138">Debe aparecer exactamente una vez para cada [**cinta. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="37d26-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="37d26-139">Los elementos de QAT se pueden agregar o quitar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="37d26-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="37d26-140">Para mantener la coherencia entre las aplicaciones de la cinta de opciones, se recomienda que el controlador de comandos *CustomizeCommandName* inicie un cuadro de diálogo de personalización de Qat.</span><span class="sxs-lookup"><span data-stu-id="37d26-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="37d26-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="37d26-141">Examples</span></span>

<span data-ttu-id="37d26-142">En el ejemplo siguiente se muestra el marcado básico para **QuickAccessToolbar**.</span><span class="sxs-lookup"><span data-stu-id="37d26-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="37d26-143">En esta sección de código se muestra la declaración del comando **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="37d26-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="37d26-144">En esta sección de código se muestra la declaración de control **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="37d26-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="37d26-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="37d26-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="37d26-146">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37d26-146">Minimum supported system</span></span><br/> | <span data-ttu-id="37d26-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37d26-147">Windows 7</span></span> |
| <span data-ttu-id="37d26-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37d26-148">Can be empty</span></span>                        | <span data-ttu-id="37d26-149">No</span><span class="sxs-lookup"><span data-stu-id="37d26-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="37d26-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37d26-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d26-151">Control de barra de herramientas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="37d26-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





