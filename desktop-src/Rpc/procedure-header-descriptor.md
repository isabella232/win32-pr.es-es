---
title: Descriptor de encabezado de procedimiento
description: El encabezado se ha ampliado varias veces a lo largo de la vida del motor de NDR. El compilador actual todavía genera encabezados diferentes en función del modo del compilador. Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488114"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="1a79a-105">Descriptor de encabezado de procedimiento</span><span class="sxs-lookup"><span data-stu-id="1a79a-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="1a79a-106">El encabezado se ha ampliado varias veces a lo largo de la vida del motor de NDR.</span><span class="sxs-lookup"><span data-stu-id="1a79a-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="1a79a-107">El compilador actual todavía genera encabezados diferentes en función del modo del compilador.</span><span class="sxs-lookup"><span data-stu-id="1a79a-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="1a79a-108">Sin embargo, los encabezados más recientes son un superconjunto de los más antiguos.</span><span class="sxs-lookup"><span data-stu-id="1a79a-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="1a79a-109">El encabezado-OI anterior</span><span class="sxs-lookup"><span data-stu-id="1a79a-109">The Old –Oi Header</span></span>

<span data-ttu-id="1a79a-110">El encabezado tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a79a-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="1a79a-111">Donde \_ el tipo de identificador<1> puede ser uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1a79a-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="1a79a-112">Hex</span><span class="sxs-lookup"><span data-stu-id="1a79a-112">Hex</span></span> | <span data-ttu-id="1a79a-113">Handle</span><span class="sxs-lookup"><span data-stu-id="1a79a-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="1a79a-114">31</span><span class="sxs-lookup"><span data-stu-id="1a79a-114">31</span></span>  | <span data-ttu-id="1a79a-115">\_genérico de enlace de FC \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="1a79a-116">32</span><span class="sxs-lookup"><span data-stu-id="1a79a-116">32</span></span>  | <span data-ttu-id="1a79a-117">\_primitiva de enlace FC \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="1a79a-118">33</span><span class="sxs-lookup"><span data-stu-id="1a79a-118">33</span></span>  | <span data-ttu-id="1a79a-119">\_controlador automático de FC \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="1a79a-120">34</span><span class="sxs-lookup"><span data-stu-id="1a79a-120">34</span></span>  | <span data-ttu-id="1a79a-121">\_identificador de devolución de llamada FC \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="1a79a-122">0</span><span class="sxs-lookup"><span data-stu-id="1a79a-122">0</span></span>   | <span data-ttu-id="1a79a-123">(identificador explícito)</span><span class="sxs-lookup"><span data-stu-id="1a79a-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="1a79a-124">Si el tipo de identificador \_<1> campo es distinto de cero, el procedimiento utiliza un identificador implícito del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="1a79a-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="1a79a-125">Vea el tema sobre [identificadores](handles.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1a79a-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="1a79a-126">Si el tipo de identificador \_<1> campo es cero, el identificador usado para el enlace es uno de los parámetros del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="1a79a-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="1a79a-127">Los identificadores explícitos pueden ser primitivos, genéricos y de contexto; el último tiene el siguiente token de FC.</span><span class="sxs-lookup"><span data-stu-id="1a79a-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="1a79a-128">Hex</span><span class="sxs-lookup"><span data-stu-id="1a79a-128">Hex</span></span> | <span data-ttu-id="1a79a-129">Handle</span><span class="sxs-lookup"><span data-stu-id="1a79a-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="1a79a-130">30</span><span class="sxs-lookup"><span data-stu-id="1a79a-130">30</span></span>  | <span data-ttu-id="1a79a-131">\_contexto de enlace FC \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="1a79a-132">Por Convención, el tipo de identificador de las interfaces DCOM es el \_ identificador automático de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="1a79a-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="1a79a-133">Las \_ marcas Oi<1> campo es una máscara de 8 bits de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1a79a-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="1a79a-134">Hex</span><span class="sxs-lookup"><span data-stu-id="1a79a-134">Hex</span></span> | <span data-ttu-id="1a79a-135">Marca</span><span class="sxs-lookup"><span data-stu-id="1a79a-135">Flag</span></span>                         | <span data-ttu-id="1a79a-136">Significado</span><span class="sxs-lookup"><span data-stu-id="1a79a-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="1a79a-137">01</span><span class="sxs-lookup"><span data-stu-id="1a79a-137">01</span></span>  | <span data-ttu-id="1a79a-138">Se \_ \_ usó el PTR completo de OI \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="1a79a-139">Utiliza el paquete de puntero completo.</span><span class="sxs-lookup"><span data-stu-id="1a79a-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="1a79a-140">02</span><span class="sxs-lookup"><span data-stu-id="1a79a-140">02</span></span>  | <span data-ttu-id="1a79a-141">\_Asignación RPCSS de OI \_ \_ usada</span><span class="sxs-lookup"><span data-stu-id="1a79a-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="1a79a-142">Utiliza el paquete de memoria RpcSs.</span><span class="sxs-lookup"><span data-stu-id="1a79a-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="1a79a-143">04</span><span class="sxs-lookup"><span data-stu-id="1a79a-143">04</span></span>  | <span data-ttu-id="1a79a-144">\_Procedimiento de objeto OI \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="1a79a-145">Un procedimiento en una interfaz de objeto.</span><span class="sxs-lookup"><span data-stu-id="1a79a-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="1a79a-146">08</span><span class="sxs-lookup"><span data-stu-id="1a79a-146">08</span></span>  | <span data-ttu-id="1a79a-147">OI \_ tiene \_ RPCFLAGS</span><span class="sxs-lookup"><span data-stu-id="1a79a-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="1a79a-148">El procedimiento tiene marcas RPC que no son cero.</span><span class="sxs-lookup"><span data-stu-id="1a79a-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="1a79a-149">10</span><span class="sxs-lookup"><span data-stu-id="1a79a-149">10</span></span>  | <span data-ttu-id="1a79a-150">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="1a79a-150">Oi\_\*</span></span>                       | <span data-ttu-id="1a79a-151">Sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="1a79a-151">Overloaded.</span></span>                              |
| <span data-ttu-id="1a79a-152">20</span><span class="sxs-lookup"><span data-stu-id="1a79a-152">20</span></span>  | <span data-ttu-id="1a79a-153">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="1a79a-153">Oi\_\*</span></span>                       | <span data-ttu-id="1a79a-154">Sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="1a79a-154">Overloaded.</span></span>                              |
| <span data-ttu-id="1a79a-155">40</span><span class="sxs-lookup"><span data-stu-id="1a79a-155">40</span></span>  | <span data-ttu-id="1a79a-156">OI \_ usar \_ nuevas \_ rutinas de inicialización \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="1a79a-157">Utiliza las rutinas de Windows NT 3.5 beta2 + init.</span><span class="sxs-lookup"><span data-stu-id="1a79a-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="1a79a-158">80</span><span class="sxs-lookup"><span data-stu-id="1a79a-158">80</span></span>  |                              | <span data-ttu-id="1a79a-159">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="1a79a-159">Unused.</span></span>                                  |



 

<span data-ttu-id="1a79a-160">Las marcas siguientes se sobrecargan.</span><span class="sxs-lookup"><span data-stu-id="1a79a-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="1a79a-161">Hex</span><span class="sxs-lookup"><span data-stu-id="1a79a-161">Hex</span></span> | <span data-ttu-id="1a79a-162">Marca</span><span class="sxs-lookup"><span data-stu-id="1a79a-162">Flag</span></span>                                    | <span data-ttu-id="1a79a-163">Significado</span><span class="sxs-lookup"><span data-stu-id="1a79a-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="1a79a-164">10</span><span class="sxs-lookup"><span data-stu-id="1a79a-164">10</span></span>  | <span data-ttu-id="1a79a-165">\_se utiliza ENcode \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="1a79a-166">Solo se usa en la selección.</span><span class="sxs-lookup"><span data-stu-id="1a79a-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="1a79a-167">20</span><span class="sxs-lookup"><span data-stu-id="1a79a-167">20</span></span>  | <span data-ttu-id="1a79a-168">descodificación \_ se \_ usa</span><span class="sxs-lookup"><span data-stu-id="1a79a-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="1a79a-169">Solo se usa en la selección.</span><span class="sxs-lookup"><span data-stu-id="1a79a-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="1a79a-170">10</span><span class="sxs-lookup"><span data-stu-id="1a79a-170">10</span></span>  | <span data-ttu-id="1a79a-171">\_Omitir \_ el \_ control de excepciones de objeto \_</span><span class="sxs-lookup"><span data-stu-id="1a79a-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="1a79a-172">Ya no se utiliza (OLE anterior).</span><span class="sxs-lookup"><span data-stu-id="1a79a-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="1a79a-173">20</span><span class="sxs-lookup"><span data-stu-id="1a79a-173">20</span></span>  | <span data-ttu-id="1a79a-174">OI \_ tiene \_ COMM \_ o \_ error</span><span class="sxs-lookup"><span data-stu-id="1a79a-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="1a79a-175">Solo en RPC sin formato, \[ COMM \_ , \_ Estado de error \] .</span><span class="sxs-lookup"><span data-stu-id="1a79a-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="1a79a-176">20</span><span class="sxs-lookup"><span data-stu-id="1a79a-176">20</span></span>  | <span data-ttu-id="1a79a-177">La OI ( \_ obj) \_ use el \_ \_ intérprete V2</span><span class="sxs-lookup"><span data-stu-id="1a79a-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="1a79a-178">Solo en DCOM, use el intérprete [**-saliente**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="1a79a-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="1a79a-179">El \_ campo marcas de rpc<4> describe cómo establecer el campo **RpcFlags** de la estructura de [**\_ mensajes RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) .</span><span class="sxs-lookup"><span data-stu-id="1a79a-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="1a79a-180">Este campo solo está presente si las \_ marcas oi<1> campo tiene OI \_ \_ RPCFLAGS establecido.</span><span class="sxs-lookup"><span data-stu-id="1a79a-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="1a79a-181">Si este campo no está presente, las marcas de RPC para el procedimiento remoto son cero.</span><span class="sxs-lookup"><span data-stu-id="1a79a-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="1a79a-182">Para el rendimiento, los intérpretes asincrónicos siempre tienen las \_ marcas rpc<4> campo presente.</span><span class="sxs-lookup"><span data-stu-id="1a79a-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="1a79a-183">El \_ campo de> proc num<2 proporciona el número de procedimiento del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="1a79a-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="1a79a-184">El \_ tamaño de la pila<2> proporciona el tamaño total de todos los parámetros de la pila, incluido este puntero o valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1a79a-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="1a79a-185">La \_ Descripción del identificador explícito \_<> campo se describe más adelante en este documento.</span><span class="sxs-lookup"><span data-stu-id="1a79a-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="1a79a-186">Este campo no está presente si el procedimiento usa un identificador implícito.</span><span class="sxs-lookup"><span data-stu-id="1a79a-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 