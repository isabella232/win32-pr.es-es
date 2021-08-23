---
title: Estructura de carga útil de Ray
description: Estructura definida por el usuario que se proporciona como argumento de entrada en una llamada TraceRay y como un parámetro inout en los tipos de sombreador que pueden tener acceso a la carga del rayo.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565635"
---
# <a name="ray-payload-structure"></a>Estructura de carga útil de Ray 

Estructura definida por el usuario que se proporciona como argumento de entrada en una llamada [**TraceRay**](traceray-function.md) y como parámetro de entrada [](closest-hit-shader.md)en los [](miss-shader.md) tipos de sombreador que pueden tener acceso a la carga de rayos, que incluyen cualquier sombreador de impacto, el más cercano y el que se pierda. [](any-hit-shader.md) Cualquier sombreador que acceda a la carga de rayos debe usar la misma estructura que la proporcionada en la **llamada a TraceRay** de origen.  Incluso si uno de estos sombreadores no hace referencia a la carga del rayo en absoluto, debe especificar la carga correspondiente como la **llamada TraceRay** de origen.

