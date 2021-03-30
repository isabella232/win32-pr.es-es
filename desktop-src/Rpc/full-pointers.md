---
title: Punteros completos
description: A diferencia de los punteros únicos, los punteros completos admiten el alias.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995359"
---
# <a name="full-pointers"></a><span data-ttu-id="390ba-103">Punteros completos</span><span class="sxs-lookup"><span data-stu-id="390ba-103">Full Pointers</span></span>

<span data-ttu-id="390ba-104">A diferencia de los punteros [únicos](unique-pointers.md) , los punteros completos admiten el alias.</span><span class="sxs-lookup"><span data-stu-id="390ba-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="390ba-105">Esto significa que varios punteros pueden hacer referencia a los mismos datos, tal y como se muestra en la ilustración siguiente:</span><span class="sxs-lookup"><span data-stu-id="390ba-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![dos punteros que hacen referencia a los mismos datos](images/prog-a02.png)

<span data-ttu-id="390ba-107">Un puntero completo tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="390ba-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="390ba-108">Puede tener el valor null.</span><span class="sxs-lookup"><span data-stu-id="390ba-108">It can have the value null.</span></span>
-   <span data-ttu-id="390ba-109">Puede cambiar de null a un valor distinto de NULL durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="390ba-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="390ba-110">Cuando el valor cambia a un valor distinto de NULL, el código auxiliar del cliente asigna una nueva memoria asignada en la devolución.</span><span class="sxs-lookup"><span data-stu-id="390ba-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="390ba-111">El programa cliente debe liberar esta memoria antes de que finalice.</span><span class="sxs-lookup"><span data-stu-id="390ba-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="390ba-112">Puede cambiar de un valor distinto de null a NULL durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="390ba-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="390ba-113">Cuando el valor cambia a NULL, la aplicación es responsable de liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="390ba-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="390ba-114">El valor puede cambiar de un valor distinto de null a otro.</span><span class="sxs-lookup"><span data-stu-id="390ba-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="390ba-115">El almacenamiento al que apunta un puntero completo puede ser accesible por otro puntero o nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="390ba-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="390ba-116">Los datos devueltos se escriben en el almacenamiento existente si el puntero no tiene el valor null.</span><span class="sxs-lookup"><span data-stu-id="390ba-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="390ba-117">Utilice el \[ [](/windows/desktop/Midl/ptr) \] atributo PTR para especificar un puntero completo, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="390ba-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="390ba-118">En este ejemplo, los parámetros *ptrName1* y *ptrName2* se definen como punteros completos a una cadena.</span><span class="sxs-lookup"><span data-stu-id="390ba-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="390ba-119">Es posible que ambos punteros señalen a la misma dirección de memoria que contiene una sola cadena.</span><span class="sxs-lookup"><span data-stu-id="390ba-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="390ba-120">\[**ptr** \] se requiere cuando se proporciona compatibilidad con los alias.</span><span class="sxs-lookup"><span data-stu-id="390ba-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="390ba-121">Sin embargo, puesto que requiere la mayor parte del procesamiento de todos los punteros disponibles en RPC, no se recomienda para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="390ba-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 