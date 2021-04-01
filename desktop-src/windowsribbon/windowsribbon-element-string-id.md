---
title: Propiedad String.Id
description: Representa el identificador único de un recurso de cadena.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Propiedad String.Id cinta de opciones de Windows
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150933"
---
# <a name="stringid-property"></a><span data-ttu-id="8d820-104">Propiedad String.Id</span><span class="sxs-lookup"><span data-stu-id="8d820-104">String.Id property</span></span>

<span data-ttu-id="8d820-105">Representa el identificador único de un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="8d820-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="8d820-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8d820-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="8d820-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d820-107">Attributes</span></span>

<span data-ttu-id="8d820-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8d820-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8d820-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d820-109">Child elements</span></span>

<span data-ttu-id="8d820-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8d820-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8d820-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8d820-111">Parent elements</span></span>



| <span data-ttu-id="8d820-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d820-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="8d820-113">**String@**</span><span class="sxs-lookup"><span data-stu-id="8d820-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8d820-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d820-114">Remarks</span></span>

<span data-ttu-id="8d820-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8d820-115">Optional.</span></span>

<span data-ttu-id="8d820-116">Puede aparecer como máximo una vez para cada elemento de [**cadena**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="8d820-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="8d820-117">El valor de **String.ID** debe ser único.</span><span class="sxs-lookup"><span data-stu-id="8d820-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="8d820-118">El identificador está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="8d820-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="8d820-119">Este elemento contiene un valor de la Unión de tipos *xs: positiveInteger* y *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="8d820-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="8d820-120">El valor se limita a un valor entero comprendido entre 2 y 59999, ambos incluidos, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="8d820-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="8d820-121">La longitud máxima es de 10 caracteres con ceros a la izquierda opcionales.</span><span class="sxs-lookup"><span data-stu-id="8d820-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="8d820-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d820-122">Examples</span></span>

<span data-ttu-id="8d820-123">En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String.ID** .</span><span class="sxs-lookup"><span data-stu-id="8d820-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="8d820-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d820-124">Requirements</span></span>



| <span data-ttu-id="8d820-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d820-125">Requirement</span></span> | <span data-ttu-id="8d820-126">Value</span><span class="sxs-lookup"><span data-stu-id="8d820-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8d820-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d820-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8d820-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d820-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8d820-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d820-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8d820-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d820-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





