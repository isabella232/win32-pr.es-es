---
title: atributo callback
description: El atributo \ callback \ declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida. Las funciones de devolución de llamada proporcionan una manera para que el servidor ejecute código en el cliente.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- atributo de devolución de llamada MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420650"
---
# <a name="callback-attribute"></a><span data-ttu-id="26e23-105">atributo callback</span><span class="sxs-lookup"><span data-stu-id="26e23-105">callback attribute</span></span>

<span data-ttu-id="26e23-106">El atributo **\[ callback \]** declara una función de devolución de llamada estática que existe en el lado cliente de la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="26e23-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="26e23-107">Las funciones de devolución de llamada proporcionan una manera para que el servidor ejecute código en el cliente.</span><span class="sxs-lookup"><span data-stu-id="26e23-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="26e23-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26e23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e23-109">*function-ATTR-List*</span><span class="sxs-lookup"><span data-stu-id="26e23-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-110">Especifica cero o más atributos que se aplican a la función.</span><span class="sxs-lookup"><span data-stu-id="26e23-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="26e23-111">Los atributos de función válidos son **\[** [**locales**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="26e23-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="26e23-112">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="26e23-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="26e23-113">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="26e23-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-114">Especifica un [ \_ tipo base](midl-base-types.md), [**un struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="26e23-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="26e23-115">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="26e23-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="26e23-116">*PTR-declarador*</span><span class="sxs-lookup"><span data-stu-id="26e23-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-117">Especifica cero o más declaradores de puntero.</span><span class="sxs-lookup"><span data-stu-id="26e23-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="26e23-118">Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="26e23-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="26e23-119">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="26e23-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-120">Especifica el nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="26e23-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="26e23-121">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="26e23-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-122">Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="26e23-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="26e23-123">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="26e23-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="26e23-124">*clara*</span><span class="sxs-lookup"><span data-stu-id="26e23-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="26e23-125">Especifica un declarador de C estándar, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="26e23-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="26e23-126">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="26e23-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="26e23-127">El identificador de nombre de parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="26e23-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26e23-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26e23-128">Remarks</span></span>

<span data-ttu-id="26e23-129">La función de **\[ devolución de llamada \]** es útil cuando el servidor debe obtener información del cliente.</span><span class="sxs-lookup"><span data-stu-id="26e23-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="26e23-130">Si se admiten aplicaciones de servidor en Windows 3. *x*, el servidor podría hacer una llamada a un procedimiento remoto en Windows 3. *x* servidor para obtener la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="26e23-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="26e23-131">La función de devolución de llamada logra el mismo propósito y permite que el servidor consulte al cliente información en el contexto de la llamada original.</span><span class="sxs-lookup"><span data-stu-id="26e23-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="26e23-132">Las devoluciones de llamada son casos especiales de llamadas remotas que se ejecutan como parte de un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="26e23-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="26e23-133">Se emite una devolución de llamada en el contexto de una llamada remota.</span><span class="sxs-lookup"><span data-stu-id="26e23-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="26e23-134">Cualquier procedimiento remoto definido como parte de la misma interfaz que la función de devolución de llamada estática puede llamar a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="26e23-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="26e23-135">Es importante tener en cuenta que no se recomienda el uso de la \[ devolución \] de llamada en la programación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="26e23-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="26e23-136">Como función de programación de un solo subproceso, no está equipada para admitir las demandas de seguridad que proporciona un entorno con varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="26e23-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="26e23-137">No se puede usar la función **RpcCancelThread** para cancelar una llamada que pueda enviar una devolución de llamada estática.</span><span class="sxs-lookup"><span data-stu-id="26e23-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="26e23-138">Si una llamada a procedimiento remoto determinada nunca dará lugar a una devolución de llamada, se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="26e23-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="26e23-139">De lo contrario, una llamada solo se puede cancelar si se puede garantizar que no se ha emitido una devolución de llamada para ella.</span><span class="sxs-lookup"><span data-stu-id="26e23-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="26e23-140">Solo las secuencias orientadas a la conexión y del protocolo local admiten el atributo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="26e23-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="26e23-141">El tamaño de los \[ datos de salida \] para las devoluciones de llamada en la secuencia de protocolo local está limitado a 150 bytes.</span><span class="sxs-lookup"><span data-stu-id="26e23-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="26e23-142">Si una interfaz RPC utiliza una secuencia de protocolo de conexión sin conexión, se producirá un error en las llamadas a procedimientos con el atributo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="26e23-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="26e23-143">Los identificadores no se pueden usar como parámetros en funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="26e23-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="26e23-144">Dado que las devoluciones de llamada siempre se ejecutan en el contexto de una llamada, el identificador de enlace utilizado por el cliente para realizar la llamada al servidor también se utiliza como identificador de enlace del servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="26e23-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="26e23-145">Las devoluciones de llamada pueden anidar a cualquier profundidad.</span><span class="sxs-lookup"><span data-stu-id="26e23-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="26e23-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26e23-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="26e23-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="26e23-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e23-148">**matrices**</span><span class="sxs-lookup"><span data-stu-id="26e23-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="26e23-149">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="26e23-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="26e23-150">**const**</span><span class="sxs-lookup"><span data-stu-id="26e23-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="26e23-151">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="26e23-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="26e23-152">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="26e23-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="26e23-153">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="26e23-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="26e23-154">**omitir**</span><span class="sxs-lookup"><span data-stu-id="26e23-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="26e23-155">**localizar**</span><span class="sxs-lookup"><span data-stu-id="26e23-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="26e23-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="26e23-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="26e23-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="26e23-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="26e23-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="26e23-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="26e23-159">**string**</span><span class="sxs-lookup"><span data-stu-id="26e23-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="26e23-160">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="26e23-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="26e23-161">**Unión**</span><span class="sxs-lookup"><span data-stu-id="26e23-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="26e23-162">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="26e23-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="26e23-163">**RpcCancelThread**</span><span class="sxs-lookup"><span data-stu-id="26e23-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 