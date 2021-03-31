---
title: Indicadores de tipo
description: Las propiedades reales siguen la tabla de identificadores de propiedad y los valores de conjunto de propiedades de pares de desplazamiento. Cada propiedad se almacena como DWORD, seguida del valor del tipo de datos.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078113"
---
# <a name="type-indicators"></a><span data-ttu-id="de956-104">Indicadores de tipo</span><span class="sxs-lookup"><span data-stu-id="de956-104">Type Indicators</span></span>

<span data-ttu-id="de956-105">Las propiedades reales siguen la tabla de identificadores de propiedad y los valores de conjunto de propiedades de pares de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="de956-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="de956-106">Cada propiedad se almacena como **DWORD**, seguida del valor del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="de956-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="de956-107">Los indicadores de tipo y sus valores asociados se describen en la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="de956-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="de956-108">Todos los pares de tipo/valor deben comenzar en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de956-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="de956-109">Por lo tanto, los valores pueden ir seguidos de bytes null para alinear el par subsiguiente en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de956-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="de956-110">En el código de ejemplo siguiente se calcula el número de bytes necesarios para alinear en un límite de 32 bits, dado un recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="de956-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="de956-111">Dentro de un vector de valores, cada repetición de un valor escalar simple menor que 32 bits debe alinearse con su alineación natural en lugar de con una alineación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de956-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="de956-112">En la práctica, esto solo es importante para los tipos **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** y **VT \_ bool** (que tienen alineación natural de un byte o dos bytes).</span><span class="sxs-lookup"><span data-stu-id="de956-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="de956-113">Todos los demás tipos tienen una alineación natural de cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="de956-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="de956-114">Algunos tipos, por ejemplo, **VT \_ R8**, tienen una alineación natural de 8 bytes, pero se almacenan como si tienen una alineación de cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="de956-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="de956-115">Un valor de propiedad con el indicador de tipo **VT \_ I2** \| **\_ VT** puede incluir:</span><span class="sxs-lookup"><span data-stu-id="de956-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="de956-116">Un recuento de elementos **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="de956-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="de956-117">Secuencia de enteros de dos bytes empaquetados sin relleno nulo entre ellos.</span><span class="sxs-lookup"><span data-stu-id="de956-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de956-118">Los recuentos de 32 bits o los tipos de propiedad que se almacenan como parte de un elemento de propiedad de vector también deben estar alineados con 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de956-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="de956-119">Un valor de propiedad de tipo identificador de tipo **VT \_ LPSTR** \| **\_ VT** puede incluir:</span><span class="sxs-lookup"><span data-stu-id="de956-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="de956-120">Un recuento de elementos **DWORD** (**DWORD** *cElems*).</span><span class="sxs-lookup"><span data-stu-id="de956-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="de956-121">Secuencia de cadenas (**Char** *rgch \[ \]*), cada una de ellas precedida de un **valor DWORD** de longitud y, posiblemente, un relleno null para redondear a un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de956-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 