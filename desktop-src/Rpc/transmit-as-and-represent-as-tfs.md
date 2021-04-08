---
title: Transmit_as y Represent_as
description: Transmitir \_ como y representan \_ como recursos compartidos del mismo diseño, excepto el token inicial; el token lee la \_ transmisión \_ de FC como o FC \_ \_ como, pero el código subyacente es común.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995296"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="59ee7-103">Transmitir \_ como y representar \_ como</span><span class="sxs-lookup"><span data-stu-id="59ee7-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="59ee7-104">Transmitir \_ como y representan \_ como recursos compartidos del mismo diseño, excepto el token inicial; el token lee la \_ transmisión \_ de FC como o FC \_ \_ como, pero el código subyacente es común.</span><span class="sxs-lookup"><span data-stu-id="59ee7-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="59ee7-105">La descripción tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="59ee7-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="59ee7-106">Las marcas<1> byte están formadas por el recorte superior de la marca y el recorte de alineación inferior.</span><span class="sxs-lookup"><span data-stu-id="59ee7-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="59ee7-107">El recorte de la alineación mantiene la alineación del cable del tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="59ee7-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="59ee7-108">Esto es necesario cuando se cambia el tamaño del búfer y se usa el tamaño del tipo transmitido desde el código de formato.</span><span class="sxs-lookup"><span data-stu-id="59ee7-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="59ee7-109">La marca de recorte puede tener las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="59ee7-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="59ee7-110">El \_ tipo presentado \_ es \_ una marca de matriz marca un argumento transmitir como (o representar como) de nivel superior como una matriz de algo y un valor pasado por.</span><span class="sxs-lookup"><span data-stu-id="59ee7-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="59ee7-111">El intérprete [**– OI**](/windows/desktop/Midl/-oi) usa esta marca para depurar este tipo de argumento (que en realidad es un puntero en Stack, no en la matriz).</span><span class="sxs-lookup"><span data-stu-id="59ee7-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="59ee7-112">Las otras dos marcas también se usan solo en intérpretes anteriores para ir correctamente sobre un tipo presentado en la pila.</span><span class="sxs-lookup"><span data-stu-id="59ee7-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="59ee7-113">El \_ Índice quíntuplo<2> es un índice de la rutina de devolución de llamada quíntuplo (es realmente un cuádruple) de funciones.</span><span class="sxs-lookup"><span data-stu-id="59ee7-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="59ee7-114">La tabla es común para transmitir como y representar como y hay una asignación obvia para la posición de las rutinas, ya que el mismo servicio de puntos de entrada transmite como y representan códigos.</span><span class="sxs-lookup"><span data-stu-id="59ee7-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="59ee7-115">La asignación es de \_ local => a la \_ transmisión, a \_ local => desde \_ transmisión, \_ inst. inst => transmisión gratuita \_ , local gratis \_ => \_ inst.</span><span class="sxs-lookup"><span data-stu-id="59ee7-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="59ee7-116">El \_ \_ \_ tamaño de memoria de tipo presentado<2> siempre proporciona un tamaño para el tipo presentado/local, incluidos los tipos de representación desconocidos.</span><span class="sxs-lookup"><span data-stu-id="59ee7-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="59ee7-117">El tamaño del búfer de tipo transmitido \_ \_ \_<2> es cero, cuando el tamaño es variable o el tamaño fijo real.</span><span class="sxs-lookup"><span data-stu-id="59ee7-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="59ee7-118">Se trata de una optimización que permite omitir algunas devoluciones de llamada al cambiar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="59ee7-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="59ee7-119">El desplazamiento de tipo transmitido \_ \_<2> es el desplazamiento de tipo relativo habitual a la cadena de formato de tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="59ee7-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 