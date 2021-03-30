---
title: Command. TooltipTitle (propiedad)
description: Representa un título de información sobre herramientas.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Command. TooltipTitle (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492509"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="7e54b-104">Command. TooltipTitle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7e54b-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="7e54b-105">Representa un título de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="7e54b-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="7e54b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7e54b-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="7e54b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e54b-107">Attributes</span></span>

<span data-ttu-id="7e54b-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7e54b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7e54b-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e54b-109">Child elements</span></span>



| <span data-ttu-id="7e54b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e54b-110">Element</span></span>                                                   | <span data-ttu-id="7e54b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e54b-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="7e54b-112">**String@**</span><span class="sxs-lookup"><span data-stu-id="7e54b-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="7e54b-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="7e54b-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7e54b-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7e54b-114">Parent elements</span></span>



| <span data-ttu-id="7e54b-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e54b-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="7e54b-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="7e54b-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7e54b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e54b-117">Remarks</span></span>

<span data-ttu-id="7e54b-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7e54b-118">Optional.</span></span>

<span data-ttu-id="7e54b-119">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="7e54b-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="7e54b-120">**Command. TooltipTitle** puede contener un valor de tipo *xs: String* restringido a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="7e54b-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="7e54b-121">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="7e54b-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="7e54b-122">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="7e54b-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="7e54b-123">Si no se proporciona ningún valor para **Command. TooltipTitle**, se requiere el elemento secundario [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="7e54b-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="7e54b-124">Si **Command. TooltipTitle** contiene un valor y un elemento secundario de [**cadena**](windowsribbon-element-string.md) , la **cadena** tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="7e54b-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="7e54b-125">**Command. TooltipTitle** solo admite la alineación izquierda.</span><span class="sxs-lookup"><span data-stu-id="7e54b-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="7e54b-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e54b-126">Examples</span></span>

<span data-ttu-id="7e54b-127">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. TooltipTitle** .</span><span class="sxs-lookup"><span data-stu-id="7e54b-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7e54b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e54b-128">Requirements</span></span>



| <span data-ttu-id="7e54b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e54b-129">Requirement</span></span> | <span data-ttu-id="7e54b-130">Value</span><span class="sxs-lookup"><span data-stu-id="7e54b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7e54b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e54b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7e54b-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e54b-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7e54b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e54b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7e54b-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e54b-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e54b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e54b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e54b-136">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="7e54b-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





