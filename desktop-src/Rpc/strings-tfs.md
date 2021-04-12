---
title: Cadenas (RPC)
description: Tres tipos de cadenas y llamada a procedimiento remoto (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359282"
---
# <a name="strings-rpc"></a><span data-ttu-id="dd7ab-103">Cadenas (RPC)</span><span class="sxs-lookup"><span data-stu-id="dd7ab-103">Strings (RPC)</span></span>

<span data-ttu-id="dd7ab-104">Hay tres tipos de cadenas que se indican mediante las siguientes subcadenas finales en el carácter de formato.</span><span class="sxs-lookup"><span data-stu-id="dd7ab-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="dd7ab-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd7ab-105">Type</span></span>                  | <span data-ttu-id="dd7ab-106">Substring</span><span class="sxs-lookup"><span data-stu-id="dd7ab-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="dd7ab-107">Cadena de caracteres</span><span class="sxs-lookup"><span data-stu-id="dd7ab-107">Character string</span></span>      | <span data-ttu-id="dd7ab-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="dd7ab-108">CSTRING</span></span>   |
| <span data-ttu-id="dd7ab-109">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="dd7ab-109">Wide character string</span></span> | <span data-ttu-id="dd7ab-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="dd7ab-110">WSTRING</span></span>   |
| <span data-ttu-id="dd7ab-111">Estructura que permite cadenas</span><span class="sxs-lookup"><span data-stu-id="dd7ab-111">String-able structure</span></span> | <span data-ttu-id="dd7ab-112">SSTRING</span><span class="sxs-lookup"><span data-stu-id="dd7ab-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="dd7ab-113">Cadenas no compatibles</span><span class="sxs-lookup"><span data-stu-id="dd7ab-113">Nonconformant Strings</span></span>

<span data-ttu-id="dd7ab-114">Un ejemplo de cadena no conforme es una **\[ cadena \]** en una matriz de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="dd7ab-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="dd7ab-115">Cadenas compatibles</span><span class="sxs-lookup"><span data-stu-id="dd7ab-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="dd7ab-116">-o bien-</span><span class="sxs-lookup"><span data-stu-id="dd7ab-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="dd7ab-117">El primer formato describe cadenas comunes, como un argumento de carácter de **\[ \] cadena** \* .</span><span class="sxs-lookup"><span data-stu-id="dd7ab-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="dd7ab-118">Una cadena compatible con tamaño tiene la última Descripción.</span><span class="sxs-lookup"><span data-stu-id="dd7ab-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="dd7ab-119">La descripción del cumplimiento \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="dd7ab-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="dd7ab-120">Cadenas de estructura</span><span class="sxs-lookup"><span data-stu-id="dd7ab-120">Structure Strings</span></span>

<span data-ttu-id="dd7ab-121">La siguiente es una estructura que permite la cadena no conforme:</span><span class="sxs-lookup"><span data-stu-id="dd7ab-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="dd7ab-122">Estructura compatible con cadenas compatibles:</span><span class="sxs-lookup"><span data-stu-id="dd7ab-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="dd7ab-123">de</span><span class="sxs-lookup"><span data-stu-id="dd7ab-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="dd7ab-124">La última Descripción es para una estructura que permita la cadena con el tamaño.</span><span class="sxs-lookup"><span data-stu-id="dd7ab-124">The latter description is for a sized string-able structure.</span></span>

 

 