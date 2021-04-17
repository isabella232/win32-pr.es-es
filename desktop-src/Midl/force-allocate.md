---
title: force_allocate atributo)
description: El atributo ACF \ Force \_ allocate \ obliga a que se asigne un parámetro de puntero mediante \_ \_ la asignación de usuarios de MIDL en lugar de optimizar la asignación.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487583"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="1327f-104">forzar \_ asignación de atributo</span><span class="sxs-lookup"><span data-stu-id="1327f-104">force\_allocate attribute</span></span>

<span data-ttu-id="1327f-105">El atributo ACF de \[ **\_ asignación forzada** \] obliga a que se asigne un parámetro de puntero mediante la asignación de [**\_ usuarios \_ de MIDL**](midl-user-allocate-1.md) en lugar de optimizar la asignación.</span><span class="sxs-lookup"><span data-stu-id="1327f-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="1327f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1327f-106">Parameters</span></span>

<span data-ttu-id="1327f-107">Este atributo no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1327f-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1327f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1327f-108">Remarks</span></span>

<span data-ttu-id="1327f-109">RPC intenta minimizar las asignaciones de memoria en el servidor mediante el suministro de punteros a los búferes de memoria internos.</span><span class="sxs-lookup"><span data-stu-id="1327f-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="1327f-110">Este enfoque puede provocar problemas en las aplicaciones que intentan llamar directamente al [**usuario de MIDL \_ \_**](midl-user-free-1.md) en punteros proporcionados por RPC, ya que no se puede liberar un puntero que se ha optimizado.</span><span class="sxs-lookup"><span data-stu-id="1327f-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="1327f-111">Marcar un parámetro con **\[ Force \_ allocate \]** impedirá esta optimización para todos los punteros que lo deriven.</span><span class="sxs-lookup"><span data-stu-id="1327f-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="1327f-112">Otro uso común de **\[ forzar \_ asignación \]** es garantizar la alineación de la memoria a la que se señala si una aplicación requiere una alineación mayor que la de la memoria a la que se apunta.</span><span class="sxs-lookup"><span data-stu-id="1327f-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="1327f-113">Por ejemplo, las aplicaciones a menudo pasan datos en una matriz genérica de bytes en lugar de usar el tipo real, pero solo se garantiza que un byte está alineado en 1, lo que puede causar problemas en las aplicaciones que suponen una alineación mayor.</span><span class="sxs-lookup"><span data-stu-id="1327f-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="1327f-114">Al marcar el parámetro con **\[ Force \_ allocate \]**, la aplicación puede garantizar que toda la memoria a la que se señala tendrá una alineación igual a la garantizada por la [**asignación de \_ usuarios \_ de MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="1327f-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1327f-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1327f-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="1327f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="1327f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1327f-117">Evitar la ocultación de información</span><span class="sxs-lookup"><span data-stu-id="1327f-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="1327f-118">Diseño de interfaces compatibles con 64 bits</span><span class="sxs-lookup"><span data-stu-id="1327f-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="1327f-119">**\_asignación de usuarios de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="1327f-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="1327f-120">**usuario de MIDL \_ \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="1327f-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="1327f-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="1327f-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 