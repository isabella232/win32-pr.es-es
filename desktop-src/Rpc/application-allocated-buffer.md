---
title: Búfer de Application-Allocated
description: El atributo ACF \ byte \_ Count \ indica al código auxiliar que use un búfer preasignado que no se haya asignado ni liberado por las rutinas de soporte técnico del cliente.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488119"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="a7df3-103">Búfer de Application-Allocated</span><span class="sxs-lookup"><span data-stu-id="a7df3-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="a7df3-104">El \[ [**\_ número de bytes**](/windows/desktop/Midl/byte-count) del atributo ACF \] indica al código auxiliar que utilice un búfer preasignado que no están asignados ni liberado por las rutinas de soporte técnico del cliente.</span><span class="sxs-lookup"><span data-stu-id="a7df3-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="a7df3-105">El \[ atributo de **\_ recuento de bytes** \] se aplica a un puntero o a un parámetro de matriz que apunta al búfer.</span><span class="sxs-lookup"><span data-stu-id="a7df3-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="a7df3-106">Requiere un parámetro que especifique el tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="a7df3-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="a7df3-107">El área de memoria asignada por el cliente puede contener estructuras de datos complejas con varios punteros.</span><span class="sxs-lookup"><span data-stu-id="a7df3-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="a7df3-108">Dado que el área de memoria es contiguo, la aplicación no tiene que realizar varias llamadas para liberar cada puntero y estructura de forma individual.</span><span class="sxs-lookup"><span data-stu-id="a7df3-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="a7df3-109">Al igual que cuando se usa el \[ atributo [**asignar (todos los \_ nodos)**](/windows/desktop/Midl/allocate) \] , el área de memoria se puede asignar o liberar con una llamada a la rutina de asignación de memoria o la rutina gratuita.</span><span class="sxs-lookup"><span data-stu-id="a7df3-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="a7df3-110">Sin embargo, a diferencia de lo que ocurre con el atributo de \[ **asignación (todos los \_ nodos)** \] , el código auxiliar del cliente no administra el parámetro de búfer, sino que la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a7df3-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="a7df3-111">El búfer debe ser un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida y la longitud del búfer en bytes debe ser un \[ [](/windows/desktop/Midl/in) \] parámetro solo en.</span><span class="sxs-lookup"><span data-stu-id="a7df3-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="a7df3-112">El \[ [**atributo \_ recuento de bytes**](/windows/desktop/Midl/byte-count) \] solo se puede aplicar a tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="a7df3-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="a7df3-113">El \[ atributo ACF de **\_ recuento de bytes** \] es una extensión de Microsoft a DCE IDL y, como tal, no está disponible si se compila con el modificador [**/OSF**](/windows/desktop/Midl/-osf) de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a7df3-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="a7df3-114">En el ejemplo siguiente, el parámetro *pRoot* utiliza el recuento de bytes:</span><span class="sxs-lookup"><span data-stu-id="a7df3-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="a7df3-115">El \[ [**atributo \_ recuento de bytes**](/windows/desktop/Midl/byte-count) \] aparece en el ACF como:</span><span class="sxs-lookup"><span data-stu-id="a7df3-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="a7df3-116">El código auxiliar de cliente generado a partir de estos archivos IDL y ACF no asigna ni libera memoria para este búfer.</span><span class="sxs-lookup"><span data-stu-id="a7df3-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="a7df3-117">El código auxiliar del servidor asigna y libera el búfer en una sola llamada utilizando el parámetro de tamaño proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a7df3-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="a7df3-118">Si los datos son demasiado grandes para el tamaño de búfer especificado, se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="a7df3-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 