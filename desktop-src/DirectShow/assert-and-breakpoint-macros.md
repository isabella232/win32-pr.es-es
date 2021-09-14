---
description: Aserción y macros de punto de interrupción
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Aserción y macros de punto de interrupción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162249"
---
# <a name="assert-and-breakpoint-macros"></a>Aserción y macros de punto de interrupción

Las [DirectShow base proporcionan](directshow-base-classes.md) varias macros que realizan aserciones o provocan puntos de interrupción.



| Macro                                        | Descripción                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**AFIRMAR**](assert.md)                     | Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es **FALSE.**                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Comprueba si un puntero está alineado con un límite especificado.                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | Muestra un cuadro de mensaje con la cadena especificada, el nombre del archivo de origen y el número de línea.                                |
| [**EXECUTE \_ ASSERT**](execute-assert.md)    | Evalúa una expresión en compilaciones de depuración y comercial. En las compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **FALSE.** |
| [**CACHESERT**](kassert.md)                   | Evalúa una expresión y produce una excepción de punto de interrupción si la expresión es **FALSE.**                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Produce una excepción de punto de interrupción y registra la cadena especificada.                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilidades de depuración](debugging-utilities.md)
</dt> </dl>

 

 



