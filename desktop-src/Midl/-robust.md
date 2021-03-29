---
title: parámetro/Robust
description: El modificador/Robust indica al compilador de MIDL que genere información adicional de comprobación de errores, que el motor de NDR utiliza para realizar comprobaciones de integridad en tiempo de ejecución.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- parámetro de modificador de/ROBUST MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904021"
---
# <a name="robust-switch"></a><span data-ttu-id="7902f-104">parámetro/Robust</span><span class="sxs-lookup"><span data-stu-id="7902f-104">/robust switch</span></span>

<span data-ttu-id="7902f-105">El modificador **/Robust** indica al compilador de MIDL que genere información adicional de comprobación de errores, que el motor de NDR utiliza para realizar comprobaciones de integridad en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7902f-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="7902f-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="7902f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="7902f-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="7902f-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="7902f-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="7902f-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="7902f-109">Estos modificadores son idénticos en su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7902f-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="7902f-110">Especifican el método proxy con código de serialización y usan cadenas de formato rápido para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7902f-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="7902f-111">Vea/ [**OI**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="7902f-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7902f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7902f-112">Remarks</span></span>

<span data-ttu-id="7902f-113">El uso del modificador **/Robust** genera información adicional que permite que el motor de representación de datos de red (NDR) realice la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y en punteros de interfaz [**out**](out-idl.md) en aplicaciones DCOM.</span><span class="sxs-lookup"><span data-stu-id="7902f-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="7902f-114">El modificador **/Robust** solo está disponible en Windows 2000 y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="7902f-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="7902f-115">Un argumento correlacionado es un argumento que utiliza cualquiera de los atributos que permiten determinar el tamaño de un objeto de datos en tiempo de ejecución: [**el tamaño \_ es**](size-is.md), la [**longitud \_ es**](length-is.md), el [**primero \_ es**](first-is.md), el [**último \_ es**](last-is.md), el de [**conmutador \_ es**](switch-is.md)y el [**IID \_ es**](iid-is.md). [**\_**](max-is.md)</span><span class="sxs-lookup"><span data-stu-id="7902f-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="7902f-116">De acuerdo con la especificación de OSF-DCE para la representación de la conexión, este argumento correlacionado aparece en dos lugares diferentes.</span><span class="sxs-lookup"><span data-stu-id="7902f-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="7902f-117">Por ejemplo, considere un uso típico del **tamaño \_ es** Attribute:</span><span class="sxs-lookup"><span data-stu-id="7902f-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="7902f-118">En este ejemplo, el cliente pasa un Long que especifica el tamaño de un bloque de tipos de barra \_ (en términos de número de \_ elementos de tipo barra) y un puntero al bloque real de tipos de barra \_ .</span><span class="sxs-lookup"><span data-stu-id="7902f-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="7902f-119">El argumento de tamaño se correlaciona con el argumento pBarType.</span><span class="sxs-lookup"><span data-stu-id="7902f-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="7902f-120">De acuerdo con la especificación de OSF-DCE, el argumento de tamaño se representa dos veces en la conexión, primero como en sí mismo y después con la matriz de elementos de tipo de barra \_ que representa el argumento pBarType.</span><span class="sxs-lookup"><span data-stu-id="7902f-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="7902f-121">No se calculan las referencias de cada argumento de forma independiente, según su propia representación de conexión.</span><span class="sxs-lookup"><span data-stu-id="7902f-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="7902f-122">Normalmente, el argumento de tamaño y su copia, que se usa para representar parte del otro argumento, tienen los mismos valores.</span><span class="sxs-lookup"><span data-stu-id="7902f-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="7902f-123">Sin embargo, si el argumento de tamaño está dañado (por ejemplo, cuando el bloque de \_ tipos de barra es mayor que el asignado), la aplicación de servidor puede dejar de responder, ya que usa el valor del argumento size para medir los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="7902f-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="7902f-124">El modificador **/Robust** es necesario para implementar una comprobación de intervalo válida con el atributo de [**intervalo**](range.md) .</span><span class="sxs-lookup"><span data-stu-id="7902f-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="7902f-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7902f-125">Examples</span></span>

<span data-ttu-id="7902f-126">**MIDL/Robust/Oicf nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="7902f-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="7902f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7902f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7902f-128">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="7902f-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7902f-129">**/OI**</span><span class="sxs-lookup"><span data-stu-id="7902f-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="7902f-130">**range**</span><span class="sxs-lookup"><span data-stu-id="7902f-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




