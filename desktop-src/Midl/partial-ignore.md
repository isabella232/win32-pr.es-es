---
title: partial_ignore atributo)
description: El atributo ACF \ \_ Ignore parcial \ define una versión especializada de los punteros \ Unique \ que proporciona la semántica opcional.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore el atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419673"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="02122-104">\_omitir el atributo parcial</span><span class="sxs-lookup"><span data-stu-id="02122-104">partial\_ignore attribute</span></span>

<span data-ttu-id="02122-105">El atributo ACF **\[ \_ Ignore \] parcial** define una versión especializada de punteros **\[ únicos \]** que proporciona la semántica opcional de salida.</span><span class="sxs-lookup"><span data-stu-id="02122-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="02122-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02122-106">Remarks</span></span>

<span data-ttu-id="02122-107">Al crear una función, es habitual permitir que los usuarios especifiquen un puntero no **nulo** a los datos devueltos opcionales, que a menudo se denominan punteros de salida opcionales.</span><span class="sxs-lookup"><span data-stu-id="02122-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="02122-108">Normalmente no es necesario inicializar la memoria a la que apunta el usuario.</span><span class="sxs-lookup"><span data-stu-id="02122-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="02122-109">Esta técnica representa un problema cuando la función se utiliza en RPC.</span><span class="sxs-lookup"><span data-stu-id="02122-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="02122-110">Si el puntero de salida opcional es válido, pero apunta a datos no inicializados, RPC intenta calcular las referencias de los datos y enviarlos al servidor, lo que puede provocar un error en el cálculo de referencias y anular la llamada.</span><span class="sxs-lookup"><span data-stu-id="02122-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="02122-111">Incluso si el cálculo de referencias se realiza correctamente, se envía al servidor una cantidad potencialmente grande de datos inútiles.</span><span class="sxs-lookup"><span data-stu-id="02122-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="02122-112">Estos problemas se resuelven marcando el puntero como **\[ in, out, Unique y \_ parcial \] Ignore**.</span><span class="sxs-lookup"><span data-stu-id="02122-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="02122-113">Los cuatro atributos deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="02122-113">All four attributes must be present.</span></span> <span data-ttu-id="02122-114">Cuando se calculan las referencias de un puntero **\[ \_ \] parcial** en el lado del cliente, los únicos datos que se envían al servidor son un indicador que muestra si el puntero es **null**.</span><span class="sxs-lookup"><span data-stu-id="02122-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="02122-115">Si el puntero no es **null**, la rutina del lado servidor recibe un puntero válido a un bloque de memoria que se ha inicializado con ceros.</span><span class="sxs-lookup"><span data-stu-id="02122-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="02122-116">Si el puntero es **null**, la rutina del lado servidor recibe un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="02122-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="02122-117">En esta situación, el tamaño máximo del puntero debe estar bien definido en tiempo de compilación o en función de los parámetros de entrada, ya que el servidor debe asignar espacio para la ubicación de memoria a la que se apunta.</span><span class="sxs-lookup"><span data-stu-id="02122-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="02122-118">Por ejemplo, un puntero de **\[ cadena \]** simple no tiene un tamaño bien definido porque la cadena termina implícitamente con un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="02122-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="02122-119">En este caso, si **\[ \_ se \]** especifica el tamaño máximo de la cadena mediante la adición de un tamaño, el atributo lograría el requisito de tamaño bien definido.</span><span class="sxs-lookup"><span data-stu-id="02122-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="02122-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="02122-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="02122-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="02122-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02122-122">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="02122-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




