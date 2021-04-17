---
title: String. Content (propiedad)
description: Representa el contenido de un recurso de cadena.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Propiedad String. Content (cinta de Windows)
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705129"
---
# <a name="stringcontent-property"></a><span data-ttu-id="cdec5-104">String. Content (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cdec5-104">String.Content property</span></span>

<span data-ttu-id="cdec5-105">Representa el contenido de un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="cdec5-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="cdec5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="cdec5-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="cdec5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdec5-107">Attributes</span></span>

<span data-ttu-id="cdec5-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="cdec5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cdec5-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdec5-109">Child elements</span></span>

<span data-ttu-id="cdec5-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="cdec5-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cdec5-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="cdec5-111">Parent elements</span></span>



| <span data-ttu-id="cdec5-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="cdec5-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="cdec5-113">**String@**</span><span class="sxs-lookup"><span data-stu-id="cdec5-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cdec5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdec5-114">Remarks</span></span>

<span data-ttu-id="cdec5-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cdec5-115">Optional.</span></span>

<span data-ttu-id="cdec5-116">Puede aparecer como máximo una vez para cada elemento de [**cadena**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="cdec5-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="cdec5-117">Este elemento contiene un valor de tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="cdec5-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="cdec5-118">El valor está restringido a una cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="cdec5-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="cdec5-119">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="cdec5-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="cdec5-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cdec5-120">Examples</span></span>

<span data-ttu-id="cdec5-121">En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String. Content** .</span><span class="sxs-lookup"><span data-stu-id="cdec5-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="cdec5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdec5-122">Requirements</span></span>



| <span data-ttu-id="cdec5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdec5-123">Requirement</span></span> | <span data-ttu-id="cdec5-124">Value</span><span class="sxs-lookup"><span data-stu-id="cdec5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="cdec5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdec5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cdec5-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdec5-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="cdec5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdec5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cdec5-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdec5-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





