---
title: String. Symbol (propiedad)
description: Representa el nombre de un recurso de cadena.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Propiedad String. Symbol de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905044"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="4d44c-104">String. Symbol (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4d44c-104">String.Symbol property</span></span>

<span data-ttu-id="4d44c-105">Representa el nombre de un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="4d44c-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="4d44c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4d44c-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="4d44c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d44c-107">Attributes</span></span>

<span data-ttu-id="4d44c-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="4d44c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4d44c-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d44c-109">Child elements</span></span>

<span data-ttu-id="4d44c-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4d44c-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4d44c-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4d44c-111">Parent elements</span></span>



| <span data-ttu-id="4d44c-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="4d44c-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="4d44c-113">**String@**</span><span class="sxs-lookup"><span data-stu-id="4d44c-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4d44c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d44c-114">Remarks</span></span>

<span data-ttu-id="4d44c-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4d44c-115">Optional.</span></span>

<span data-ttu-id="4d44c-116">Puede aparecer como máximo una vez para cada elemento de [**cadena**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="4d44c-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="4d44c-117">El símbolo está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="4d44c-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="4d44c-118">Este elemento contiene un valor de tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="4d44c-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="4d44c-119">El valor está restringido a una cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="4d44c-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="4d44c-120">La longitud máxima es de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d44c-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="4d44c-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d44c-121">Examples</span></span>

<span data-ttu-id="4d44c-122">En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="4d44c-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="4d44c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d44c-123">Requirements</span></span>



| <span data-ttu-id="4d44c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d44c-124">Requirement</span></span> | <span data-ttu-id="4d44c-125">Value</span><span class="sxs-lookup"><span data-stu-id="4d44c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4d44c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d44c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4d44c-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d44c-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4d44c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d44c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4d44c-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d44c-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





