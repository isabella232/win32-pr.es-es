---
title: Registro de Regístrese
description: Este registro de salida del sombreador de vértices contiene un color de vértice por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974279"
---
# <a name="fog-register"></a>Registro de Regístrese

Este registro de salida del sombreador de vértices contiene un color de vértice por vértice.

Un registro consta de propiedades que determinan cómo se comporta cada registro.



| Propiedad        | Descripción                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nombre            | oFog                                                                                            |
| Count           | Un vector, del que solo se puede usar un componente y debe especificarse mediante la máscara de componente |
| Permisos de E/S | De solo escritura.                                                                                     |



 

El valor de salida se registra. El valor es el factor de curva que se va a interpolar y, a continuación, se enruta a la tabla de tablas. Solo se usa el componente x escalar de la zona.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




