---
title: Estructura de carga útil de Ray
description: Estructura definida por el usuario que se proporciona como argumento de entrada en una llamada TraceRay y como un parámetro inout en los tipos de sombreador que pueden tener acceso a la carga del rayo.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072911"
---
# <a name="ray-payload-structure"></a>Estructura de carga útil de Ray 

Estructura definida por el usuario que se proporciona como argumento de entrada en una llamada [**TraceRay**](traceray-function.md) y como parámetro de entrada [](closest-hit-shader.md)en los [](miss-shader.md) tipos de sombreador que pueden tener acceso a la carga de rayos, que incluyen cualquier sombreador de impacto, el más cercano y el que se pierda. [](any-hit-shader.md) Cualquier sombreador que acceda a la carga de rayos debe usar la misma estructura que la proporcionada en la **llamada a TraceRay** de origen.  Incluso si uno de estos sombreadores no hace referencia a la carga del rayo en absoluto, debe especificar la carga correspondiente como la **llamada TraceRay** de origen.

