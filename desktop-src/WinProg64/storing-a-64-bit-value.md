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
# <a name="storing-a-64-bit-value"></a>Almacenar un valor de 64 bits

Para almacenar un valor de puntero de 64 bits, utilice **ULong \_ ptr**. Un valor **ULong \_ PTR** es 32 bits cuando se compila con un compilador de 32 bits y 64 bits cuando se compila con un compilador de 64 bits.

En los ejemplos siguientes se usa el código del mundo real que se ha trasladado a Windows de 64 bits. Comentario sobre los pasos para que se incluya el código compatible con 64 bits.

## <a name="example-1-getting-an-address"></a>Ejemplo 1: obtener una dirección

En el código siguiente se muestra una manera portátil de obtener una dirección.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Usar ULONG (un método solo de 32 bits)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>Usar ULONG_PTR (el método portable)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>Ejemplo 2: calcular una dirección

En el código siguiente se muestra una manera portátil de calcular una dirección.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Usar ULONG (un método solo de 32 bits)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>Usar ULONG_PTR (el método portable)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




