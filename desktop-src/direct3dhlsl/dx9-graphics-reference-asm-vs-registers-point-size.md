---
title: Registro de tamaño de punto
description: Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119669"
---
# <a name="point-size-register"></a>Registro de tamaño de punto

Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértice.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamaño de punto    | x    | x    | x     | x    | x    | x     |



 

Un registro consta de propiedades que determinan cómo se comporta cada registro.



| Propiedad        | Descripción                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nombre            | Opta                                                                                            |
| Count           | 1 vector, del que solo se puede usar un componente y debe especificarse mediante la máscara de componente. |
| Permisos de E/S | De solo escritura.                                                                                     |



 

Solo se usa el componente x escalar del tamaño de punto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




