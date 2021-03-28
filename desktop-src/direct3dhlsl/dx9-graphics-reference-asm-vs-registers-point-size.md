---
title: Registro de tamaño de punto
description: Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértices.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418612"
---
# <a name="point-size-register"></a>Registro de tamaño de punto

Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértices.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamaño de punto    | x    | x    | x     | x    | x    | x     |



 

Un registro consta de propiedades que determinan el comportamiento de cada registro.



| Propiedad        | Descripción                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nombre            | Aporta                                                                                            |
| Count           | 1 Vector, del que solo se puede usar un componente y debe especificarse mediante la máscara del componente. |
| Permisos de e/s | De solo escritura.                                                                                     |



 

Solo se usa el componente x escalar del tamaño de punto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




