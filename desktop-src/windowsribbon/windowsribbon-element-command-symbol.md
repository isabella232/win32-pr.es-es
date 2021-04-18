---
title: Command. Symbol (propiedad)
description: Representa el nombre de un comando al que se puede hacer referencia externamente.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Command. Symbol (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705172"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="7bc1c-104">Command. Symbol (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7bc1c-104">Command.Symbol property</span></span>

<span data-ttu-id="7bc1c-105">Representa el nombre de un [**comando**](windowsribbon-element-command.md) al que se puede hacer referencia externamente.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="7bc1c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7bc1c-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="7bc1c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7bc1c-107">Attributes</span></span>

<span data-ttu-id="7bc1c-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7bc1c-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7bc1c-109">Child elements</span></span>

<span data-ttu-id="7bc1c-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7bc1c-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7bc1c-111">Parent elements</span></span>



| <span data-ttu-id="7bc1c-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="7bc1c-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="7bc1c-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="7bc1c-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7bc1c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bc1c-114">Remarks</span></span>

<span data-ttu-id="7bc1c-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-115">Optional.</span></span>

<span data-ttu-id="7bc1c-116">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="7bc1c-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="7bc1c-117">El símbolo está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="7bc1c-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="7bc1c-118">Este elemento contiene un valor de tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="7bc1c-119">El valor está restringido a una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos y caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="7bc1c-120">La longitud máxima es de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="7bc1c-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7bc1c-121">Examples</span></span>

<span data-ttu-id="7bc1c-122">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="7bc1c-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7bc1c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bc1c-123">Requirements</span></span>



| <span data-ttu-id="7bc1c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bc1c-124">Requirement</span></span> | <span data-ttu-id="7bc1c-125">Value</span><span class="sxs-lookup"><span data-stu-id="7bc1c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7bc1c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bc1c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc1c-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bc1c-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7bc1c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bc1c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc1c-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bc1c-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





