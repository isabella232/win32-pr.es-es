---
title: idempotente (atributo)
description: El atributo \ idempotente \ especifica que una operación no modifica información de estado y devuelve los mismos resultados cada vez que se realiza. Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- atributo idempotente (MIDL)
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532602"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="02871-105">idempotente (atributo)</span><span class="sxs-lookup"><span data-stu-id="02871-105">idempotent attribute</span></span>

<span data-ttu-id="02871-106">El atributo **\[ idempotente \]** especifica que una operación no modifica la información de estado y devuelve los mismos resultados cada vez que se realiza.</span><span class="sxs-lookup"><span data-stu-id="02871-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="02871-107">Realizar la rutina más de una vez tiene el mismo efecto que realizarla una vez.</span><span class="sxs-lookup"><span data-stu-id="02871-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="02871-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02871-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02871-109">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="02871-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-110">Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="02871-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="02871-111">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="02871-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="02871-112">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="02871-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-113">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="02871-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="02871-114">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="02871-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-115">Especifica los atributos adicionales que se van a aplicar a la función.</span><span class="sxs-lookup"><span data-stu-id="02871-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="02871-116">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="02871-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="02871-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="02871-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-118">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="02871-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="02871-119">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="02871-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-120">Especifica el nombre de la función a la que se aplicará el atributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="02871-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="02871-121">*params*</span><span class="sxs-lookup"><span data-stu-id="02871-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="02871-122">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="02871-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02871-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02871-123">Remarks</span></span>

<span data-ttu-id="02871-124">RPC admite dos tipos de semántica de llamadas remotas: llama a las operaciones con el atributo **\[ idempotente \]** y llama a las operaciones (operaciones *idempotente* ) sin el atributo **\[ idempotente \]** (operaciones *no idempotente* ).</span><span class="sxs-lookup"><span data-stu-id="02871-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="02871-125">Una operación idempotente se puede llevar a cabo más de una vez sin ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="02871-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="02871-126">Por el contrario, una operación no idempotente no se puede ejecutar más de una vez, ya que devolverá resultados diferentes cada vez o porque modificará algún Estado.</span><span class="sxs-lookup"><span data-stu-id="02871-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="02871-127">Para asegurarse de que un procedimiento se vuelve a ejecutar automáticamente si la llamada no se completa, utilice el atributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="02871-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="02871-128">Si los atributos **\[ idempotente \]**, **\[** [**Broadcast**](broadcast.md) **\]** o **\[** [**maybe**](maybe.md) **\]** no están presentes, el procedimiento usará la semántica no idempotente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="02871-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="02871-129">En este caso, la operación se ejecuta solo una vez.</span><span class="sxs-lookup"><span data-stu-id="02871-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="02871-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="02871-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02871-131">**amplia**</span><span class="sxs-lookup"><span data-stu-id="02871-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="02871-132">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="02871-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="02871-133">**incluso**</span><span class="sxs-lookup"><span data-stu-id="02871-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




