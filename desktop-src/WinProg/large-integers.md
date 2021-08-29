---
title: Enteros grandes
description: Las funciones y estructuras de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en valores de 32 Windows.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- enteros grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7266b36f7e6a6efb11eaa2d73d752f03e46e3f9d022637558fe6b04db8e8ee4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859135"
---
# <a name="large-integers"></a>Enteros grandes

Las funciones y estructuras de enteros grandes proporcionaron originalmente compatibilidad con valores de 64 bits en valores de 32 Windows. Ahora, el compilador de C puede admitir enteros de 64 bits de forma nativa. Por ejemplo, Microsoft Visual C++ admite el tipo entero de tamaño [**\_ \_ int64.**](/windows/desktop/Midl/--int64) Para obtener más información, vea la documentación incluida con el compilador de C.

Para obtener información sobre los enteros de 64 bits en Windows de 64 bits, vea [Los nuevos tipos de datos](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Operaciones de enteros grandes

Las aplicaciones pueden multiplicar enteros de 32 bits con o sin signo, lo que genera resultados de 64 bits mediante las funciones [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) y [**UInt32x32To64.**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) Las aplicaciones pueden desplazar bits en valores de 64 bits a la izquierda o a la derecha mediante las funciones [**Int64ShllMod32,**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32) [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)e [**Int64ShrlMod32.**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) Estas funciones proporcionan desplazamiento lógico y aritmético.

Las aplicaciones también pueden multiplicar y dividir valores de 32 bits en una sola operación mediante la [**función MulDiv.**](/windows/desktop/api/Winbase/nf-winbase-muldiv) Aunque el resultado de la operación es un valor de 32 bits, la función almacena el resultado intermedio como un valor de 64 bits, por lo que no se pierde información cuando se multiplican y dividen valores grandes de 32 bits.

## <a name="large-integer-reference"></a>Referencia de enteros grandes

-   [Funciones de entero grande](large-integer-functions.md)
-   [Estructuras de enteros grandes](large-integer-structures.md)

 

 