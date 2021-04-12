---
title: Almacenar un valor de 64 bits
description: Para almacenar un valor de puntero de 64 bits, utilice ULONG \_ PTR. Un \_ valor ulong PTR es 32 bits cuando se compila con un compilador de 32 bits y 64 bits cuando se compila con un compilador de 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- almacenar valores de 64 bits programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357111"
---
# <a name="storing-a-64-bit-value"></a><span data-ttu-id="8cabe-105">Almacenar un valor de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8cabe-105">Storing a 64-bit Value</span></span>

<span data-ttu-id="8cabe-106">Para almacenar un valor de puntero de 64 bits, utilice **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="8cabe-106">To store a 64-bit pointer value, use **ULONG\_PTR**.</span></span> <span data-ttu-id="8cabe-107">Un valor **ULong \_ PTR** es 32 bits cuando se compila con un compilador de 32 bits y 64 bits cuando se compila con un compilador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8cabe-107">A **ULONG\_PTR** value is 32 bits when compiled with a 32-bit compiler and 64 bits when compiled with a 64-bit compiler.</span></span>

<span data-ttu-id="8cabe-108">En los ejemplos siguientes se usa el código del mundo real que se ha trasladado a Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8cabe-108">The following examples use real-world code that has been ported to 64-bit Windows.</span></span> <span data-ttu-id="8cabe-109">Comentario sobre los pasos para que se incluya el código compatible con 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8cabe-109">Commentary on the steps to make the code 64-bit compatible is included.</span></span>

## <a name="example-1-getting-an-address"></a><span data-ttu-id="8cabe-110">Ejemplo 1: obtener una dirección</span><span class="sxs-lookup"><span data-stu-id="8cabe-110">Example 1: Getting an Address</span></span>

<span data-ttu-id="8cabe-111">En el código siguiente se muestra una manera portátil de obtener una dirección.</span><span class="sxs-lookup"><span data-stu-id="8cabe-111">The following code illustrates a portable way to get an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cabe-112">Usar ULONG (un método solo de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="8cabe-112">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cabe-113">Usar ULONG_PTR (el método portable)</span><span class="sxs-lookup"><span data-stu-id="8cabe-113">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a><span data-ttu-id="8cabe-114">Ejemplo 2: calcular una dirección</span><span class="sxs-lookup"><span data-stu-id="8cabe-114">Example 2: Calculating an Address</span></span>

<span data-ttu-id="8cabe-115">En el código siguiente se muestra una manera portátil de calcular una dirección.</span><span class="sxs-lookup"><span data-stu-id="8cabe-115">The following code illustrates a portable way to calculate an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cabe-116">Usar ULONG (un método solo de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="8cabe-116">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cabe-117">Usar ULONG_PTR (el método portable)</span><span class="sxs-lookup"><span data-stu-id="8cabe-117">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




