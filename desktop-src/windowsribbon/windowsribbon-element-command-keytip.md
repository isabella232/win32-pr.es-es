---
title: Command. KeyTip (propiedad)
description: Representa el KeyTip de un control.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Command. KeyTip (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705177"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="b07e0-104">Command. KeyTip (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b07e0-104">Command.Keytip property</span></span>

<span data-ttu-id="b07e0-105">Representa el KeyTip de un control.</span><span class="sxs-lookup"><span data-stu-id="b07e0-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="b07e0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="b07e0-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="b07e0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b07e0-107">Attributes</span></span>

<span data-ttu-id="b07e0-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b07e0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b07e0-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b07e0-109">Child elements</span></span>



| <span data-ttu-id="b07e0-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b07e0-110">Element</span></span>                                                   | <span data-ttu-id="b07e0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b07e0-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b07e0-112">**String@**</span><span class="sxs-lookup"><span data-stu-id="b07e0-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="b07e0-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="b07e0-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b07e0-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b07e0-114">Parent elements</span></span>



| <span data-ttu-id="b07e0-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="b07e0-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="b07e0-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="b07e0-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b07e0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b07e0-117">Remarks</span></span>

<span data-ttu-id="b07e0-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b07e0-118">Optional.</span></span>

<span data-ttu-id="b07e0-119">Puede producirse una vez como máximo para cada elemento [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="b07e0-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="b07e0-120">**Command. KeyTip** puede contener un valor de tipo *xs: String* restringido a cualquier secuencia de caracteres Unicode, incluido el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="b07e0-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="b07e0-121">Un **comando. KeyTip** solo puede empezar con un número cuando está asociado a un control en una [pestaña](windowsribbon-controls-tab.md) o en la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="b07e0-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="b07e0-122">Para mostrar las keytips que son válidas para el estado actual de la cinta de opciones, mantenga presionada la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="b07e0-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="b07e0-123">En la captura de pantalla siguiente se muestran las keytips iniciales, o el primer nivel, que se muestran en Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b07e0-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="b07e0-124">Una vez que se ha seleccionado un KeyTip de primer nivel, solo se muestran las keytips de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="b07e0-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![keytips de primer nivel en Microsoft Paint para Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="b07e0-126">**Command. KeyTip** actúa como la tecla de aceleración de un comando, a menos que ese comando se exponga a través de un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="b07e0-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="b07e0-127">En este caso, el marco de trabajo omite el valor de **Command. KeyTip** y usa un carácter precedido por una y comercial según lo especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b07e0-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="b07e0-128">Si no se especifica el carácter de y comercial mediante la etiqueta **Command. LabelTitle** o UI \_ PKEY \_ , no se expone ningún KeyTip ni tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="b07e0-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="b07e0-129">Si no se proporciona ningún valor para **Command. KeyTip**, se requiere el elemento secundario de [**cadena**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="b07e0-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="b07e0-130">Si **Command. KeyTip** contiene un valor y un elemento secundario de [**cadena**](windowsribbon-element-string.md) , la **cadena** tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="b07e0-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="b07e0-131">De forma predeterminada, el marco de trabajo usa las siguientes letras para generar automáticamente keytips:</span><span class="sxs-lookup"><span data-stu-id="b07e0-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="b07e0-132">**F** está asignado al menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="b07e0-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="b07e0-133">**Y** se asigna a cualquier comando que no tenga un KeyTip especificado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b07e0-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="b07e0-134">**Z** se asigna a cada control de [Grupo](windowsribbon-controls-group.md) y no se puede personalizar.</span><span class="sxs-lookup"><span data-stu-id="b07e0-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="b07e0-135">Un KeyTip de grupo solo se muestra cuando el [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) del control especifica una opción de tamaño de **elemento emergente** .</span><span class="sxs-lookup"><span data-stu-id="b07e0-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="b07e0-136">Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="b07e0-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="b07e0-137">Ninguna de estas letras está reservada por el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b07e0-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="b07e0-138">Cada una de ellas se puede asignar a uno o varios comandos, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b07e0-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="b07e0-139">El marco de trabajo resuelve los conflictos de KeyTip de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="b07e0-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="b07e0-140">Si uno o más controles de [ficha](windowsribbon-controls-tab.md) están asociados al mismo KeyTip, se anexa un número a cada KeyTip, empezando por 1 y aumentando secuencialmente (2, 3,...) para cada control en el orden de declaración.</span><span class="sxs-lookup"><span data-stu-id="b07e0-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="b07e0-141">Si a algún control de ficha se le asigna la letra F como KeyTip, al [menú aplicación](windowsribbon-controls-applicationmenu.md) se le asigna F1 con las keytips restantes ajustadas como se describe.</span><span class="sxs-lookup"><span data-stu-id="b07e0-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="b07e0-142">Cuando se asocia a un solo control dentro de una [pestaña](windowsribbon-controls-tab.md), el KeyTip F es válido para el menú de control y la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="b07e0-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="b07e0-143">El KeyTip del menú de la aplicación predeterminado no cambia, pero se da prioridad al control en la pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="b07e0-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="b07e0-144">Si uno o más controles de una [pestaña](windowsribbon-controls-tab.md) están asociados al mismo KeyTip, el marco de trabajo refactoriza automáticamente las keytips de esos controles, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b07e0-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="b07e0-145">Una ligera variación en el color del texto se usa para resaltar las keytips refactorizadas en una implementación de la cinta de opciones estándar.</span><span class="sxs-lookup"><span data-stu-id="b07e0-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="b07e0-146">En el caso de una implementación de cinta no estándar en la que se ha personalizado el color de la cinta de opciones, este comportamiento del marco de trabajo se invalida y todas las keytips se muestran con el mismo color de texto.</span><span class="sxs-lookup"><span data-stu-id="b07e0-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="b07e0-147">Para obtener más información, vea [personalizar los colores de la cinta](ribbon-color.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="b07e0-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="b07e0-148">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="b07e0-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="b07e0-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b07e0-149">Examples</span></span>

<span data-ttu-id="b07e0-150">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. KeyTip** .</span><span class="sxs-lookup"><span data-stu-id="b07e0-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="b07e0-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b07e0-151">Requirements</span></span>



| <span data-ttu-id="b07e0-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b07e0-152">Requirement</span></span> | <span data-ttu-id="b07e0-153">Value</span><span class="sxs-lookup"><span data-stu-id="b07e0-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b07e0-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b07e0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b07e0-155">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b07e0-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b07e0-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b07e0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b07e0-157">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b07e0-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b07e0-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="b07e0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07e0-159">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="b07e0-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





