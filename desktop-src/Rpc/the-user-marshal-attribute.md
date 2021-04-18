---
title: El atributo user_marshal
description: El atributo \ User \_ Marshal \ es un atributo de tipo ACF similar en sintaxis a \ representarse \_ como \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, atributos, user_marshal llamada a procedimiento remoto
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488066"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="bb294-105">Atributo User \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="bb294-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="bb294-106">El \[ atributo [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] es un atributo de tipo ACF similar en sintaxis para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="bb294-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="bb294-107">Al igual que con el atributo IDL, las \[ [ \_ referencias de cable](/windows/desktop/Midl/wire-marshal) \] ofrecen una manera más eficaz de calcular las referencias de los datos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="bb294-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="bb294-108">Como atributo ACF, el **\[ \_ cálculo de \] referencias de usuario** permite calcular las referencias de tipos de datos personalizados que son desconocidos para MIDL.</span><span class="sxs-lookup"><span data-stu-id="bb294-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="bb294-109">Cada tipo específico de la aplicación tiene un tipo de transmisión correspondiente que define la representación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="bb294-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="bb294-110">El tipo específico de la aplicación puede ser un tipo simple, compuesto o de puntero.</span><span class="sxs-lookup"><span data-stu-id="bb294-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="bb294-111">La restricción principal es que la instancia de tipo debe tener un tamaño de memoria fijo y bien definido.</span><span class="sxs-lookup"><span data-stu-id="bb294-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="bb294-112">Si el tamaño de la instancia de tipo debe cambiar, use un campo de puntero en lugar de una matriz compatible.</span><span class="sxs-lookup"><span data-stu-id="bb294-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="bb294-113">Como alternativa, puede definir un puntero al tipo modificable.</span><span class="sxs-lookup"><span data-stu-id="bb294-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="bb294-114">Al igual que con el atributo de **\[ \_ serialización \] de conexión** , se proporcionan rutinas para el ajuste de tamaño, el cálculo de referencias, la unserialización y la liberación.</span><span class="sxs-lookup"><span data-stu-id="bb294-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="bb294-115">En la tabla siguiente se describen los cuatro nombres de rutina proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bb294-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="bb294-116"><type>Es el *tipo* de userm especificado en la definición del tipo de **\[ cálculo de \_ referencias \] del usuario** .</span><span class="sxs-lookup"><span data-stu-id="bb294-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="bb294-117">Rutina</span><span class="sxs-lookup"><span data-stu-id="bb294-117">Routine</span></span>                                                            | <span data-ttu-id="bb294-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb294-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="bb294-119"><type>\_Usuarios</span><span class="sxs-lookup"><span data-stu-id="bb294-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="bb294-120">Ajusta el tamaño del búfer de datos RPC antes de calcular las referencias en el cliente o el servidor.</span><span class="sxs-lookup"><span data-stu-id="bb294-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="bb294-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="bb294-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="bb294-122">Calcula las referencias de los datos en el lado cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="bb294-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="bb294-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="bb294-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="bb294-124">Anula las referencias de los datos en el lado cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="bb294-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="bb294-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="bb294-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="bb294-126">Libera los datos en el lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb294-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="bb294-127">Estas rutinas proporcionadas por el usuario las proporciona el cliente o la aplicación de servidor, en función de los atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="bb294-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="bb294-128">Si el parámetro es \[ solo [en](/windows/desktop/Midl/in) \] , el cliente se transmite al servidor.</span><span class="sxs-lookup"><span data-stu-id="bb294-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="bb294-129">El cliente necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="bb294-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="bb294-130">El servidor necesita las funciones **<type> \_ UserUnmarshal** y **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="bb294-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="bb294-131">Para un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida, el servidor se transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="bb294-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="bb294-132">El servidor necesita las funciones **<type> \_ users** y **<type> \_ UserMarshal** , mientras que el cliente necesita la función **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="bb294-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb294-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb294-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb294-134">Atributo de \_ serialización de cable</span><span class="sxs-lookup"><span data-stu-id="bb294-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="bb294-135">Serialización de reglas para serialización de usuario y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="bb294-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="bb294-136">\_serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="bb294-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="bb294-137">\_serialización de cable</span><span class="sxs-lookup"><span data-stu-id="bb294-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="bb294-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="bb294-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 