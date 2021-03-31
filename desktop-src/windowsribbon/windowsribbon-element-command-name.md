---
title: Propiedad Command.Name
description: Representa el nombre de un comando.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Propiedad Command.Name cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079666"
---
# <a name="commandname-property"></a><span data-ttu-id="9c0d3-104">Propiedad Command.Name</span><span class="sxs-lookup"><span data-stu-id="9c0d3-104">Command.Name property</span></span>

<span data-ttu-id="9c0d3-105">Representa el nombre de un comando.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-105">Represents the name of a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="9c0d3-106">Uso</span><span class="sxs-lookup"><span data-stu-id="9c0d3-106">Usage</span></span>

``` syntax
<Command.Name/>
```

## <a name="attributes"></a><span data-ttu-id="9c0d3-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c0d3-107">Attributes</span></span>

<span data-ttu-id="9c0d3-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9c0d3-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c0d3-109">Child elements</span></span>

<span data-ttu-id="9c0d3-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9c0d3-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9c0d3-111">Parent elements</span></span>



| <span data-ttu-id="9c0d3-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c0d3-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="9c0d3-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="9c0d3-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9c0d3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c0d3-114">Remarks</span></span>

<span data-ttu-id="9c0d3-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-115">Optional.</span></span>

<span data-ttu-id="9c0d3-116">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="9c0d3-117">Se hace referencia a **Command.Name** en el marcado para asociar un comando a un control mediante el atributo *CommandName* del control.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-117">**Command.Name** is referenced in markup to associate a Command with a control through the *CommandName* attribute of the control.</span></span>

<span data-ttu-id="9c0d3-118">Este elemento contiene un valor de tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="9c0d3-119">El valor está restringido a una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos y caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="9c0d3-120">La longitud máxima es de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="9c0d3-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c0d3-121">Examples</span></span>

<span data-ttu-id="9c0d3-122">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command.Name** .</span><span class="sxs-lookup"><span data-stu-id="9c0d3-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Name** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9c0d3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c0d3-123">Requirements</span></span>



| <span data-ttu-id="9c0d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c0d3-124">Requirement</span></span> | <span data-ttu-id="9c0d3-125">Value</span><span class="sxs-lookup"><span data-stu-id="9c0d3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9c0d3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c0d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0d3-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9c0d3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c0d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0d3-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





