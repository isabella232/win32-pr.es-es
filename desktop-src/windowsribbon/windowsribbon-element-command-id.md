---
title: Propiedad Command.Id
description: Representa un identificador único para un comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Propiedad Command.Id cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492532"
---
# <a name="commandid-property"></a><span data-ttu-id="93622-104">Propiedad Command.Id</span><span class="sxs-lookup"><span data-stu-id="93622-104">Command.Id property</span></span>

<span data-ttu-id="93622-105">Representa un identificador único para un comando.</span><span class="sxs-lookup"><span data-stu-id="93622-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="93622-106">Uso</span><span class="sxs-lookup"><span data-stu-id="93622-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="93622-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="93622-107">Attributes</span></span>

<span data-ttu-id="93622-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="93622-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="93622-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93622-109">Child elements</span></span>

<span data-ttu-id="93622-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="93622-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="93622-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="93622-111">Parent elements</span></span>



| <span data-ttu-id="93622-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="93622-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="93622-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="93622-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="93622-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93622-114">Remarks</span></span>

<span data-ttu-id="93622-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="93622-115">Optional.</span></span>

<span data-ttu-id="93622-116">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="93622-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="93622-117">El identificador está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="93622-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="93622-118">Este elemento contiene un valor de la Unión de tipos *xs: positiveInteger* y *xs: String* restringido a un valor entero comprendido entre 2 y 59999, ambos incluidos, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="93622-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="93622-119">La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales.</span><span class="sxs-lookup"><span data-stu-id="93622-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="93622-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="93622-120">Examples</span></span>

<span data-ttu-id="93622-121">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command.ID** .</span><span class="sxs-lookup"><span data-stu-id="93622-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="93622-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93622-122">Requirements</span></span>



| <span data-ttu-id="93622-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93622-123">Requirement</span></span> | <span data-ttu-id="93622-124">Value</span><span class="sxs-lookup"><span data-stu-id="93622-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="93622-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93622-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93622-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="93622-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="93622-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93622-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93622-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="93622-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





