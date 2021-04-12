---
title: atributo de canalización
description: El constructor de tipo de canalización permite transmitir un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- atributo de canalización MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358849"
---
# <a name="pipe-attribute"></a><span data-ttu-id="4dc33-104">atributo de canalización</span><span class="sxs-lookup"><span data-stu-id="4dc33-104">pipe attribute</span></span>

<span data-ttu-id="4dc33-105">El constructor de tipo de **canalización** permite transmitir un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="4dc33-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="4dc33-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dc33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc33-107">*tipo de elemento*</span><span class="sxs-lookup"><span data-stu-id="4dc33-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc33-108">Define el tamaño de un único elemento en el búfer de transferencia.</span><span class="sxs-lookup"><span data-stu-id="4dc33-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="4dc33-109">El tipo *de elemento* puede ser un [tipo base](midl-base-types.md), un tipo predefinido \_ , un [**struct**](struct.md), una [**enumeración 32B**](v1-enum.md)o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="4dc33-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="4dc33-110">Se aplican varias restricciones a los *\_ tipos de elemento*, como se describe en la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="4dc33-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="4dc33-111">*declarador de canalización*</span><span class="sxs-lookup"><span data-stu-id="4dc33-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc33-112">Especifica uno o más identificadores o punteros a los identificadores.</span><span class="sxs-lookup"><span data-stu-id="4dc33-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="4dc33-113">Separe varios declaradores con comas.</span><span class="sxs-lookup"><span data-stu-id="4dc33-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dc33-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dc33-114">Remarks</span></span>

<span data-ttu-id="4dc33-115">Puede usar el constructor de tipo de **canalización** para transmitir datos en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="4dc33-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="4dc33-116">Un **\[** [](in.md) **\]** parámetro in Pipe permite al servidor extraer el flujo de datos del cliente durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="4dc33-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="4dc33-117">Un **\[** parámetro [**out**](out-idl.md) **\]** Pipe permite que el servidor devuelva la secuencia de datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="4dc33-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="4dc33-118">Proporcione las rutinas del lado cliente para insertar y extraer el flujo de datos y para asignar un búfer global para los datos.</span><span class="sxs-lookup"><span data-stu-id="4dc33-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="4dc33-119">Las rutinas de código auxiliar de cliente y servidor calculan las referencias de los datos y no las calculan y pasan una referencia al búfer de nuevo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dc33-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="4dc33-120">Las restricciones siguientes se aplican a las canalizaciones:</span><span class="sxs-lookup"><span data-stu-id="4dc33-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="4dc33-121">Un elemento de canalización no puede ser o contener un puntero, una matriz ajustada o variable, un identificador o un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="4dc33-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="4dc33-122">Además, en la implementación de canalizaciones de Microsoft, un elemento de canalización no puede ser ni contener una [**Unión**](union.md), una [**enumeración de 16B**](enum.md)o una [**\_ \_ int3264**](--int3264.md).</span><span class="sxs-lookup"><span data-stu-id="4dc33-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="4dc33-123">No se pueden aplicar los **\[** atributos [**transmitir \_ como**](transmit-as.md) **\]** , **\[** [**representar \_ como**](represent-as.md) **\]** , **\[** [**\_ serialización de conexión**](wire-marshal.md) **\]** o cálculo de **\[** [**\_ referencias de usuario**](user-marshal.md) **\]** a un tipo de canalización o a un tipo *de elemento*.</span><span class="sxs-lookup"><span data-stu-id="4dc33-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="4dc33-124">Un tipo de canalización no puede ser un miembro de una estructura o Unión, el destino de un puntero o el tipo base de una matriz.</span><span class="sxs-lookup"><span data-stu-id="4dc33-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="4dc33-125">Un tipo de datos declarado como un tipo de canalización solo se puede usar como parámetro de una llamada remota.</span><span class="sxs-lookup"><span data-stu-id="4dc33-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="4dc33-126">Puede pasar un parámetro de canalización en cualquier dirección por valor o por referencia (puntero de referencia **\[** [](ref.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="4dc33-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="4dc33-127">Sin embargo, no se puede aplicar el **\[** [](ptr.md) **\]** atributo PTR a una canalización que se pasa por referencia.</span><span class="sxs-lookup"><span data-stu-id="4dc33-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="4dc33-128">No se puede especificar un parámetro de canalización con un **\[** puntero [**único**](unique.md) **\]** o completo, independientemente de la dirección.</span><span class="sxs-lookup"><span data-stu-id="4dc33-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="4dc33-129">No se pueden usar canalizaciones en interfaces de **\[** [**objeto**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4dc33-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="4dc33-130">No se puede aplicar el **\[** [](idempotent.md) **\]** atributo idempotente a una rutina que tenga un parámetro de canalización.</span><span class="sxs-lookup"><span data-stu-id="4dc33-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="4dc33-131">No puede usar los atributos de serialización, **\[** [**codificar**](encode.md) **\]** y **\[** [**descodificar**](decode.md) **\]** con canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="4dc33-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="4dc33-132">No se pueden usar identificadores automáticos, de forma predeterminada, ni con el atributo de **\[** [**\_ control automático**](auto-handle.md) **\]** , con canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="4dc33-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="4dc33-133">El compilador MIDL solo admite canalizaciones en modo [**/OIF**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc33-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="4dc33-134">Para obtener más información sobre cómo implementar rutinas con parámetros de canalización, vea [canalizaciones](/windows/desktop/Rpc/pipes) en la guía y referencia del programador de RPC.</span><span class="sxs-lookup"><span data-stu-id="4dc33-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="4dc33-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4dc33-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="4dc33-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc33-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc33-137">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="4dc33-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="4dc33-138">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="4dc33-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4dc33-139">**descodificar**</span><span class="sxs-lookup"><span data-stu-id="4dc33-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="4dc33-140">**codificar**</span><span class="sxs-lookup"><span data-stu-id="4dc33-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="4dc33-141">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="4dc33-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4dc33-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="4dc33-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="4dc33-143">**de**</span><span class="sxs-lookup"><span data-stu-id="4dc33-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="4dc33-144">**objeto**</span><span class="sxs-lookup"><span data-stu-id="4dc33-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="4dc33-145">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="4dc33-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4dc33-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4dc33-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="4dc33-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="4dc33-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="4dc33-148">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="4dc33-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="4dc33-149">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="4dc33-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4dc33-150">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="4dc33-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="4dc33-151">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="4dc33-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="4dc33-152">**\_serialización de usuario**</span><span class="sxs-lookup"><span data-stu-id="4dc33-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="4dc33-153">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="4dc33-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 