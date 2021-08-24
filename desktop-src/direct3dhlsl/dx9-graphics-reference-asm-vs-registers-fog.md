---
title: Registro de bosque
description: Este registro de salida del sombreador de vértices contiene un color de vértice por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6aeaea0e51960f8f4bf768b855ac31236b2bb330cfda3390fd9e61dab4ec1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854585"
---
# <a name="fog-register"></a>Registro de bosque

Este registro de salida del sombreador de vértices contiene un color de vértice por vértice.

Un registro consta de propiedades que determinan cómo se comporta cada registro.



| Propiedad        | Descripción                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nombre            | oFog                                                                                            |
| Count           | Un vector, del que solo se puede usar un componente y que debe especificarse mediante la máscara de componente |
| Permisos de E/S | De solo escritura.                                                                                     |



 

El valor de salida se registra. El valor es el factor de curva que se va a interpolar y, a continuación, se enruta a la tabla de nubes. Solo se usa el componente x escalar del rayo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




