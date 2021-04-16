---
title: Punteros de referencia de Out-Only insertados
description: Punteros de referencia de Out-Only insertados
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676473"
---
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="69d0d-103">Punteros de referencia de Out-Only insertados</span><span class="sxs-lookup"><span data-stu-id="69d0d-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="69d0d-104">Cuando se usan \[ [](/windows/desktop/Midl/out-idl) \] punteros de referencia de solo salida en Microsoft RPC, el código auxiliar del servidor generado asigna solo el primer nivel de punteros accesible desde el puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="69d0d-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="69d0d-105">Los punteros en niveles más profundos no se asignan mediante el código auxiliar, sino que deben asignarse mediante el nivel de aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="69d0d-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="69d0d-106">Por ejemplo, supongamos que una interfaz especifica una \[  \] matriz de punteros de referencia de solo salida:</span><span class="sxs-lookup"><span data-stu-id="69d0d-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="69d0d-107">En este ejemplo, el código auxiliar del servidor asigna memoria para 10 punteros y establece el valor de cada puntero en NULL.</span><span class="sxs-lookup"><span data-stu-id="69d0d-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="69d0d-108">La aplicación de servidor debe asignar la memoria para los 10 enteros [**cortos**](/windows/desktop/Midl/short) a los que hacen referencia los punteros y, a continuación, establecer los 10 punteros para que apunten a los enteros.</span><span class="sxs-lookup"><span data-stu-id="69d0d-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="69d0d-109">Cuando la \[ [](/windows/desktop/Midl/out-idl) \] estructura de datos de solo salida incluye punteros de referencia anidados, el código auxiliar del servidor asigna solo el primer puntero accesible desde el puntero de referencia.</span><span class="sxs-lookup"><span data-stu-id="69d0d-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="69d0d-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="69d0d-110">For example:</span></span>

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

<span data-ttu-id="69d0d-111">En el ejemplo anterior, el código auxiliar del servidor asigna el puntero *psTop* y **el \_ \_ tipo de struct** de estructura superior.</span><span class="sxs-lookup"><span data-stu-id="69d0d-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="69d0d-112">El puntero de referencia *PS1* del **\_ \_ tipo Top de struct** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="69d0d-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="69d0d-113">El código auxiliar del servidor no asigna todos los niveles de la estructura de datos, ni asigna **el \_ tipo STRUCT1** ni su puntero incrustado, *psValue*.</span><span class="sxs-lookup"><span data-stu-id="69d0d-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 