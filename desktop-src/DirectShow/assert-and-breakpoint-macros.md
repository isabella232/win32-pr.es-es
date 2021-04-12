---
description: Macros Assert y Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert y Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152612"
---
# <a name="assert-and-breakpoint-macros"></a>Macros Assert y Breakpoint

Las [clases base de DirectShow](directshow-base-classes.md) proporcionan varias macros que realizan aserciones o causan puntos de interrupción.



| Macro                                        | Descripción                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**DECLARAR**](assert.md)                     | Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es **falsa**.                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Comprueba si un puntero está alineado con un límite especificado.                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de código fuente y el número de línea.                                |
| [**EJECUTAR \_ aserción**](execute-assert.md)    | Evalúa una expresión en las compilaciones de depuración y comerciales. En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **falsa**. |
| [**KASSERT**](kassert.md)                   | Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es **falsa**.                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Produce una excepción de punto de interrupción y registra la cadena especificada.                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de depuración](debugging-utilities.md)
</dt> </dl>

 

 



