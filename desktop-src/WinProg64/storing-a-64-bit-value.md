---
title: Almacenar un valor de 64 bits
description: Para almacenar un valor de puntero de 64 bits, use ULONG \_ PTR. Un valor ULONG PTR es de 32 bits cuando se compila con un compilador de 32 bits y 64 bits cuando se compila con un compilador de \_ 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- almacenar valores de 64 bits de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476124"
---
# <a name="storing-a-64-bit-value"></a>Almacenar un valor de 64 bits

Para almacenar un valor de puntero de 64 bits, use **ULONG \_ PTR**. Un **valor \_ ULONG PTR** es de 32 bits cuando se compila con un compilador de 32 bits y 64 bits cuando se compila con un compilador de 64 bits.

En los ejemplos siguientes se usa código real que se ha portado a archivos de 64 Windows. Se incluye un comentario sobre los pasos para que el código sea compatible con 64 bits.

## <a name="example-1-getting-an-address"></a>Ejemplo 1: Obtener una dirección

El código siguiente muestra una manera portátil de obtener una dirección.




| | | Uso de ULONG (un método de solo 32 bits) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Uso ULONG_PTR (el método portable) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Ejemplo 2: Calcular una dirección

En el código siguiente se muestra una manera portátil de calcular una dirección.




| | | Uso de ULONG (un método de solo 32 bits) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Uso ULONG_PTR (el método portable) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




