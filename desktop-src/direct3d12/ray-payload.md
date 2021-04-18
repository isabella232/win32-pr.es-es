---
title: Estructura de la carga de Ray
description: Una estructura definida por el usuario que se proporciona como un argumento INOUT en una llamada TraceRay y como un parámetro INOUT en los tipos de sombreador que pueden tener acceso a la carga de rayo.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105707516"
---
# <a name="ray-payload-structure"></a>Estructura de la carga de Ray 

Una estructura definida por el usuario que se proporciona como un argumento INOUT en una llamada a [**TraceRay**](traceray-function.md) , y como un parámetro INOUT en los tipos de sombreador que pueden tener acceso a la carga de rayo, que incluye [cualquier golpe](any-hit-shader.md), el [golpe más cercano](closest-hit-shader.md)y los sombreadores de [errores](miss-shader.md) . Los sombreadores que tengan acceso a la carga de rayo deben usar la misma estructura que la proporcionada en la llamada **TraceRay** de origen.  Incluso si uno de estos sombreadores no hace referencia a la carga de Ray, todavía debe especificar la carga de coincidencia como la llamada **TraceRay** de origen.

