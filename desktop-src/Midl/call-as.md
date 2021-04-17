---
title: call_as (atributo)
description: El atributo \ Call \_ as \ permite asignar una función a la que no se puede llamar de forma remota a una función remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as el atributo MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651338"
---
# <a name="call_as-attribute"></a><span data-ttu-id="3d00b-104">llamar a \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="3d00b-104">call\_as attribute</span></span>

<span data-ttu-id="3d00b-105">El atributo **\[ Call \_ as \]** permite asignar una función a la que no se puede llamar de forma remota a una función remota.</span><span class="sxs-lookup"><span data-stu-id="3d00b-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="3d00b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d00b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d00b-107">*procedimiento local*</span><span class="sxs-lookup"><span data-stu-id="3d00b-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="3d00b-108">Especifica una rutina definida por la operación.</span><span class="sxs-lookup"><span data-stu-id="3d00b-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="3d00b-109">*operación-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="3d00b-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d00b-110">Especifica uno o más atributos que se aplican a la operación.</span><span class="sxs-lookup"><span data-stu-id="3d00b-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="3d00b-111">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="3d00b-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3d00b-112">*nombre de operación*</span><span class="sxs-lookup"><span data-stu-id="3d00b-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3d00b-113">Especifica la operación con nombre que se presenta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d00b-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d00b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d00b-114">Remarks</span></span>

<span data-ttu-id="3d00b-115">La capacidad de asignar una función a la que no se puede llamar de forma remota a una función remota es especialmente útil en las interfaces que tienen numerosos tipos de parámetro que no se pueden transmitir a través de la red.</span><span class="sxs-lookup"><span data-stu-id="3d00b-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="3d00b-116">En lugar de usar muchos **\[** [**representan \_ como**](represent-as.md) **\]** y **\[** [**transmitir \_ como**](transmit-as.md) **\]** tipos, puede combinar todas las conversiones mediante las rutinas **\[ Call \_ as \]** .</span><span class="sxs-lookup"><span data-stu-id="3d00b-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="3d00b-117">Proporcione las dos **\[ llamadas \_ como \]** rutinas (lado cliente y servidor) para enlazar la rutina entre las llamadas a la aplicación y las llamadas remotas.</span><span class="sxs-lookup"><span data-stu-id="3d00b-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="3d00b-118">El atributo **\[ Call \_ as \]** se puede usar para las interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="3d00b-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="3d00b-119">En este caso, la definición de la interfaz se puede usar para las llamadas locales, así como para las llamadas remotas, ya que la **\[ llamada \_ as \]** permite que una interfaz a la que no se puede tener acceso de forma remota se asigne de manera transparente a una interfaz remota.</span><span class="sxs-lookup"><span data-stu-id="3d00b-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="3d00b-120">El atributo **\[ Call \_ as \]** no se puede usar con el modo [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="3d00b-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="3d00b-121">Por ejemplo, supongamos que la rutina **F1** en la interfaz de objeto **IFace** requiere numerosas conversiones entre las llamadas del usuario y lo que realmente se transmite.</span><span class="sxs-lookup"><span data-stu-id="3d00b-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="3d00b-122">En los ejemplos siguientes se describen los archivos IDL y ACF de la interfaz **IFace**:</span><span class="sxs-lookup"><span data-stu-id="3d00b-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="3d00b-123">En el archivo IDL de la interfaz **IFace**:</span><span class="sxs-lookup"><span data-stu-id="3d00b-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="3d00b-124">En ACF para la interfaz **IFace**:</span><span class="sxs-lookup"><span data-stu-id="3d00b-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="3d00b-125">Esto hace que el archivo de encabezado generado defina la interfaz utilizando la definición de **F1**, pero también proporciona códigos auxiliares para **Remf1**.</span><span class="sxs-lookup"><span data-stu-id="3d00b-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="3d00b-126">El compilador MIDL generará la siguiente tabla vtable en el archivo de encabezado de la interfaz **IFace**:</span><span class="sxs-lookup"><span data-stu-id="3d00b-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="3d00b-127">Después, el proxy del lado cliente tendría un proxy generado por MIDL típico para **Remf1**, mientras que el código auxiliar del lado servidor para **Remf1** sería el mismo que el código auxiliar típico generado por MIDL:</span><span class="sxs-lookup"><span data-stu-id="3d00b-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="3d00b-128">A continuación, se deben codificar manualmente las dos **\[ llamadas \_ como \]** rutinas de enlace (lado cliente y servidor):</span><span class="sxs-lookup"><span data-stu-id="3d00b-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="3d00b-129">En el caso de las interfaces de objeto, estos son los prototipos para las rutinas de enlace.</span><span class="sxs-lookup"><span data-stu-id="3d00b-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="3d00b-130">Para el lado cliente:</span><span class="sxs-lookup"><span data-stu-id="3d00b-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="3d00b-131">En el lado del servidor:</span><span class="sxs-lookup"><span data-stu-id="3d00b-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="3d00b-132">En el caso de las interfaces que no son de objeto, estos son los prototipos de las rutinas de Bond.</span><span class="sxs-lookup"><span data-stu-id="3d00b-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="3d00b-133">Para el lado cliente:</span><span class="sxs-lookup"><span data-stu-id="3d00b-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="3d00b-134">En el lado del servidor:</span><span class="sxs-lookup"><span data-stu-id="3d00b-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="3d00b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d00b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d00b-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="3d00b-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="3d00b-137">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="3d00b-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="3d00b-138">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="3d00b-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




