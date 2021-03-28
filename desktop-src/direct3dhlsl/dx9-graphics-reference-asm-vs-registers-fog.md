---
title: Registro de niebla
description: Este registro de salida del sombreador de vértices contiene un color de niebla por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983711"
---
# <a name="fog-register"></a>Registro de niebla

Este registro de salida del sombreador de vértices contiene un color de niebla por vértice.

Un registro consta de propiedades que determinan el comportamiento de cada registro.



| Propiedad        | Descripción                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nombre            | oFog                                                                                            |
| Count           | Un vector, del que solo se puede usar un componente y que debe especificar la máscara de componente. |
| Permisos de e/s | De solo escritura.                                                                                     |



 

El valor de niebla de salida se registra. El valor es el factor de niebla que se va a interpolar y, a continuación, enrutar a la tabla de niebla. Solo se usa el componente x escalar de la niebla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




