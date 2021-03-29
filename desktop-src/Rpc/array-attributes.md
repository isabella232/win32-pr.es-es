---
title: Atributos de matriz
description: Hay una relación de cierre entre las matrices y los punteros en el lenguaje C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793227"
---
# <a name="array-attributes"></a><span data-ttu-id="19a92-103">Atributos de matriz</span><span class="sxs-lookup"><span data-stu-id="19a92-103">Array Attributes</span></span>

<span data-ttu-id="19a92-104">Hay una relación de cierre entre las matrices y los punteros en el lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="19a92-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="19a92-105">Cuando se pasa como un parámetro a una función, el nombre de una matriz se trata como un puntero al primer elemento de la matriz, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="19a92-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="19a92-106">En una llamada local, puede usar el parámetro de puntero a marzo a través de la memoria y examinar el contenido de otras direcciones:</span><span class="sxs-lookup"><span data-stu-id="19a92-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="19a92-107">Cuando un cliente pasa un puntero a un procedimiento remoto, el código auxiliar del cliente transmite el puntero y los datos a los que señala.</span><span class="sxs-lookup"><span data-stu-id="19a92-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="19a92-108">A menos que el puntero esté restringido a sus datos correspondientes, toda la memoria del cliente se debe transmitir con cada llamada remota.</span><span class="sxs-lookup"><span data-stu-id="19a92-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="19a92-109">Al exigir un establecimiento de tipos seguros en la definición de interfaz, MIDL limita el procesamiento de código auxiliar de cliente a los datos correspondientes al puntero especificado.</span><span class="sxs-lookup"><span data-stu-id="19a92-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="19a92-110">El tamaño de la matriz y el intervalo de elementos de la matriz transmitidos al equipo remoto pueden ser constantes o variables.</span><span class="sxs-lookup"><span data-stu-id="19a92-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="19a92-111">Cuando estos valores son variables y, por tanto, se determinan en tiempo de ejecución, debe utilizar atributos en el archivo IDL para especificar el número de elementos de matriz que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="19a92-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="19a92-112">Los siguientes atributos de MIDL admiten límites de matriz.</span><span class="sxs-lookup"><span data-stu-id="19a92-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="19a92-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="19a92-113">Attribute</span></span>                             | <span data-ttu-id="19a92-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="19a92-114">Description</span></span>                                             | <span data-ttu-id="19a92-115">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="19a92-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="19a92-116">\[el [ **primero \_ es**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="19a92-117">Índice del primer elemento de la matriz transmitido.</span><span class="sxs-lookup"><span data-stu-id="19a92-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="19a92-118">0</span><span class="sxs-lookup"><span data-stu-id="19a92-118">0</span></span>       |
| <span data-ttu-id="19a92-119">\[[ **última \_ es**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="19a92-120">Índice del último elemento de la matriz transmitido.</span><span class="sxs-lookup"><span data-stu-id="19a92-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="19a92-121">\[la [ **longitud \_ es**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="19a92-122">Número total de elementos de matriz transmitidos.</span><span class="sxs-lookup"><span data-stu-id="19a92-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="19a92-123">\[[ **Max \_ es**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="19a92-124">Valor de índice de matriz válido más alto.</span><span class="sxs-lookup"><span data-stu-id="19a92-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="19a92-125">\[[ **min \_ es**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="19a92-126">Valor de índice de matriz válido más bajo.</span><span class="sxs-lookup"><span data-stu-id="19a92-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="19a92-127">0</span><span class="sxs-lookup"><span data-stu-id="19a92-127">0</span></span>       |
| <span data-ttu-id="19a92-128">\[[ **el tamaño \_ es**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="19a92-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="19a92-129">Número total de elementos de matriz asignados a la matriz.</span><span class="sxs-lookup"><span data-stu-id="19a92-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="19a92-130">El atributo **min \_ is** no se implementa en RPC.</span><span class="sxs-lookup"><span data-stu-id="19a92-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="19a92-131">El índice mínimo de la matriz siempre se trata como cero.</span><span class="sxs-lookup"><span data-stu-id="19a92-131">The minimum array index is always treated as zero.</span></span>

 

 

 