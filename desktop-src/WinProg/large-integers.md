---
title: Enteros grandes
description: Las estructuras y funciones de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en Windows de 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- enteros grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705015"
---
# <a name="large-integers"></a>Enteros grandes

Las estructuras y funciones de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en Windows de 32 bits. Ahora, el compilador de C puede admitir enteros de 64 bits de forma nativa. Por ejemplo, Microsoft Visual C++ admite el tipo de entero con tamaño [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Para obtener más información, vea la documentación incluida en el compilador de C.

Para obtener información sobre los enteros de 64 bits en Windows de 64 bits, consulte [los nuevos tipos de datos](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Operaciones de enteros grandes

Las aplicaciones pueden multiplicar enteros de 32 bits con signo o sin signo, generando resultados de 64 bits, mediante las funciones [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) y [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) . Las aplicaciones pueden cambiar los bits de los valores de 64 bits a la izquierda o a la derecha mediante las funciones [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)y [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) . Estas funciones proporcionan el desplazamiento aritmético y lógico.

Las aplicaciones también pueden multiplicar y dividir los valores de 32 bits en una sola operación mediante la función [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) . Aunque el resultado de la operación es un valor de 32 bits, la función almacena el resultado intermedio como un valor de 64 bits, de modo que la información no se pierde cuando se multiplican y dividen valores grandes de 32 bits.

## <a name="large-integer-reference"></a>Referencia de entero grande

-   [Funciones de enteros grandes](large-integer-functions.md)
-   [Estructuras de enteros grandes](large-integer-structures.md)

 

 