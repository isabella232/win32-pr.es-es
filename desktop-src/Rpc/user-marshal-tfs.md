---
title: Serialización de usuario
description: 'Usuario: serialización en llamada a procedimiento remoto (RPC).'
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903472"
---
# <a name="user-marshal"></a><span data-ttu-id="64475-103">Serialización de usuario</span><span class="sxs-lookup"><span data-stu-id="64475-103">User-marshal</span></span>

<span data-ttu-id="64475-104">La serialización de usuario tiene una cadena de formato similar a transmitir \_ como:</span><span class="sxs-lookup"><span data-stu-id="64475-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="64475-105">Las marcas<1> byte están formadas por el recorte superior de la marca y el recorte de alineación inferior.</span><span class="sxs-lookup"><span data-stu-id="64475-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="64475-106">Los 2 bits superiores del recorte de la marca se usan para describir si el tipo de conexión se define como un puntero único, un puntero de referencia o ningún puntero (no puede ser un PTR).</span><span class="sxs-lookup"><span data-stu-id="64475-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="64475-107">Los siguientes manifiestos se han definido para establecer u obtener las marcas:</span><span class="sxs-lookup"><span data-stu-id="64475-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="64475-108">El recorte de alineación de la palabra de marca mantiene la alineación del cable del tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="64475-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="64475-109">El \_ Índice quadruple<2> es un índice de la rutina de devolución de llamada cuádruple de las funciones de cálculo de referencias de usuario.</span><span class="sxs-lookup"><span data-stu-id="64475-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="64475-110">Las posiciones de rutina son las siguientes: el ajuste de tamaño, serialización, desserialización y liberación de rutina.</span><span class="sxs-lookup"><span data-stu-id="64475-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="64475-111">El \_ \_ \_ tamaño de memoria de tipo de usuario<2> proporciona un tamaño para el tipo específico del usuario, incluidos los tipos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="64475-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="64475-112">El tamaño del búfer de tipo transmitido \_ \_ \_<2> es cero cuando el tamaño es variable o el tamaño fijo real.</span><span class="sxs-lookup"><span data-stu-id="64475-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="64475-113">Se trata de una optimización que permite a MIDL omitir las devoluciones de llamada al cambiar el tamaño del búfer y también cuando se libera.</span><span class="sxs-lookup"><span data-stu-id="64475-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="64475-114">Intervalo</span><span class="sxs-lookup"><span data-stu-id="64475-114">Range</span></span>

<span data-ttu-id="64475-115">La \[ comprobación de intervalo \] proporciona medios adicionales para la validación de argumentos en la capa de NDR.</span><span class="sxs-lookup"><span data-stu-id="64475-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="64475-116">El \[ \] descriptor de intervalo tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="64475-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="64475-117">Las marcas toman el recorte superior y el tipo el recorte inferior del segundo byte.</span><span class="sxs-lookup"><span data-stu-id="64475-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="64475-118">Los valores bajo y alto dependen del tipo de variable que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="64475-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="64475-119">Las marcas están diseñadas como vehículo de expansión; el compilador ha establecido el recorte en cero.</span><span class="sxs-lookup"><span data-stu-id="64475-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




