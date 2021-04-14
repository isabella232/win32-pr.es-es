---
title: Command. Comment (propiedad)
description: Representa un comentario, o anotación, para un comando.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Command. Comment (propiedad, cinta de Windows)
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422543"
---
# <a name="commandcomment-property"></a><span data-ttu-id="41c84-104">Command. Comment (propiedad)</span><span class="sxs-lookup"><span data-stu-id="41c84-104">Command.Comment property</span></span>

<span data-ttu-id="41c84-105">Representa un comentario, o anotación, para un comando.</span><span class="sxs-lookup"><span data-stu-id="41c84-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="41c84-106">Uso</span><span class="sxs-lookup"><span data-stu-id="41c84-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="41c84-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="41c84-107">Attributes</span></span>

<span data-ttu-id="41c84-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="41c84-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="41c84-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41c84-109">Child elements</span></span>

<span data-ttu-id="41c84-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="41c84-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="41c84-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="41c84-111">Parent elements</span></span>



| <span data-ttu-id="41c84-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="41c84-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="41c84-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="41c84-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="41c84-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c84-114">Remarks</span></span>

<span data-ttu-id="41c84-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="41c84-115">Optional.</span></span>

<span data-ttu-id="41c84-116">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="41c84-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="41c84-117">El comentario está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="41c84-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="41c84-118">Este elemento contiene un valor de tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="41c84-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="41c84-119">La longitud máxima es de 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="41c84-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="41c84-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41c84-120">Examples</span></span>

<span data-ttu-id="41c84-121">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. Comment** .</span><span class="sxs-lookup"><span data-stu-id="41c84-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="41c84-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c84-122">Requirements</span></span>



| <span data-ttu-id="41c84-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c84-123">Requirement</span></span> | <span data-ttu-id="41c84-124">Value</span><span class="sxs-lookup"><span data-stu-id="41c84-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="41c84-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41c84-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="41c84-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="41c84-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41c84-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="41c84-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





