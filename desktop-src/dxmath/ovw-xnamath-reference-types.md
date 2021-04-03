---
description: La biblioteca de DirectXMath proporciona una serie de estructuras y tipos definidos para encapsular los datos para admitir la facilidad de uso, la optimización y la portabilidad.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Tipos de biblioteca de DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908408"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="4d8a8-103">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4d8a8-103">DirectXMath Library types</span></span>

<span data-ttu-id="4d8a8-104">La biblioteca de DirectXMath proporciona una serie de estructuras y tipos definidos para encapsular los datos para admitir la facilidad de uso, la optimización y la portabilidad.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="4d8a8-105">La lista siguiente incluye las estructuras que actualmente forman parte de la biblioteca de DirectXMath y están disponibles a través del encabezado DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4d8a8-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4d8a8-106">In this section</span></span>



| <span data-ttu-id="4d8a8-107">Tema</span><span class="sxs-lookup"><span data-stu-id="4d8a8-107">Topic</span></span>                                                             | <span data-ttu-id="4d8a8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d8a8-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d8a8-109">**MEDIO, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="4d8a8-110">Alias para **UInt16 \_ t** empaquetado con un número de punto flotante de 16 bits que consta de un bit de signo, un exponente sesgado de 5 bits y una mantisa de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="4d8a8-111">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="4d8a8-112">Tipo portable que se usa para representar un vector de componentes de punto flotante de 4 32 bits o enteros, cada uno alineado de manera óptima y asignado a un registro de vector de hardware.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="4d8a8-113">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="4d8a8-114">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8a8-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="4d8a8-115">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="4d8a8-116">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores enteros en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4d8a8-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="4d8a8-117">**XMVECTORU32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="4d8a8-118">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores UInt32 t en una instancia de tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="4d8a8-119">**XMVECTORU8, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d8a8-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="4d8a8-120">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores de Uint8 t en una instancia de tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="4d8a8-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="4d8a8-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d8a8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d8a8-122">Referencia de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4d8a8-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




