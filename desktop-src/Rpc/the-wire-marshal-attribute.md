---
title: El atributo wire_marshal
description: El atributo \ WIRE \_ Marshal \ es un atributo de tipo IDL similar en sintaxis a \ transmitir \_ como \, pero proporcionando una manera más eficaz de calcular las referencias de los datos a través de una red.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, atributos, wire_marshal llamada a procedimiento remoto
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421109"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="f052c-105">Atributo de \_ serialización de cable</span><span class="sxs-lookup"><span data-stu-id="f052c-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="f052c-106">El \[ atributo de [ \_ serialización de conexión](/windows/desktop/Midl/wire-marshal) \] es un atributo de tipo IDL similar en sintaxis para \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] , pero proporcionando una manera más eficaz de calcular las referencias de los datos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="f052c-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="f052c-107">El atributo de \[ **\_ serialización** de la conexión se usa \] para especificar un tipo de datos que se transmitirá en lugar del tipo de datos específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f052c-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="f052c-108">Cada tipo específico de la aplicación tiene un tipo de transmisión correspondiente que define la representación de la conexión (la representación usada en la red). No es necesario que el tipo específico de la aplicación sea transmitible, pero debe ser un tipo que MIDL reconozca.</span><span class="sxs-lookup"><span data-stu-id="f052c-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="f052c-109">Para calcular las referencias de un tipo desconocido a MIDL, use el atributo ACF \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="f052c-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="f052c-110">El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero.</span><span class="sxs-lookup"><span data-stu-id="f052c-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="f052c-111">La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido.</span><span class="sxs-lookup"><span data-stu-id="f052c-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="f052c-112">Si el tamaño de la instancia de tipo debe cambiar, use un campo de puntero en lugar de una matriz compatible.</span><span class="sxs-lookup"><span data-stu-id="f052c-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="f052c-113">Como alternativa, puede definir un puntero al tipo modificable.</span><span class="sxs-lookup"><span data-stu-id="f052c-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="f052c-114">Debe proporcionar las rutinas para el ajuste de tamaño, la serialización y la serialización de los datos, así como la liberación de la memoria asociada.</span><span class="sxs-lookup"><span data-stu-id="f052c-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="f052c-115">En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f052c-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="f052c-116"><type>Es el tipo de userm especificado en la definición de tipo de \[ **\_ serialización de cable** \] .</span><span class="sxs-lookup"><span data-stu-id="f052c-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="f052c-117">Rutina</span><span class="sxs-lookup"><span data-stu-id="f052c-117">Routine</span></span>                                                            | <span data-ttu-id="f052c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f052c-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="f052c-119"><type>\_Usuarios</span><span class="sxs-lookup"><span data-stu-id="f052c-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="f052c-120">Ajusta el tamaño del búfer de datos RPC antes de calcular las referencias en el cliente o el servidor.</span><span class="sxs-lookup"><span data-stu-id="f052c-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="f052c-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="f052c-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="f052c-122">Calcula las referencias de los datos en el lado cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="f052c-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="f052c-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="f052c-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="f052c-124">Anula las referencias de los datos en el lado cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="f052c-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="f052c-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="f052c-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="f052c-126">Libera los datos en el lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="f052c-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="f052c-127">Estas rutinas proporcionadas por el programador las proporciona el cliente o la aplicación de servidor en función de los atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="f052c-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="f052c-128">Si el parámetro es \[ solo [en](/windows/desktop/Midl/in) \] , el cliente se transmite al servidor.</span><span class="sxs-lookup"><span data-stu-id="f052c-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="f052c-129">El cliente necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="f052c-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="f052c-130">El servidor necesita las funciones **<type> \_ UserUnmarshal** y **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="f052c-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="f052c-131">Para un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida, el servidor se transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="f052c-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="f052c-132">El servidor necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** , mientras que el cliente necesita la función **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="f052c-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f052c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f052c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f052c-134">Atributo User \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="f052c-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="f052c-135">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="f052c-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="f052c-136">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="f052c-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="f052c-137">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="f052c-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="f052c-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="f052c-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 