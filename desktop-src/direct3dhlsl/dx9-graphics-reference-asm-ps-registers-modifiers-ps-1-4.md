---
title: ps \_ 1 \_ 4 source register modifiers for texld, texcrd
description: Las instrucciones de dirección de textura de la versión 1 4 del sombreador de dos \_ píxeles, regld - ps \_ 1 4 y \_ texcrd - ps, tienen sintaxis personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63a0cfd212767a0219af83d734d3562edacc84901098afcf77c786d8895f32d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512881"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>ps \_ 1 \_ 4 source register modifiers for texld, texcrd

Las instrucciones de dirección de textura de la versión 1 4 del sombreador de dos \_ píxeles, [regld - ps \_ 1 \_ 4](texld---ps-1-4.md) y [texcrd - ps](texcrd---ps.md), tienen sintaxis personalizada. Estas instrucciones admiten su propio conjunto de modificadores de registro de origen, selectores de registro de origen y máscaras de escritura de registro de destino, como se muestra aquí.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificadores de registro de origen para regld y texcrd

Estos modificadores proporcionan funcionalidad de división projective dividiendo los valores x e y entre los valores z o w.



| Modificadores de registro de origen | Descripción                | Sintaxis       |
|---------------------------|----------------------------|--------------|
| \_Dz                      | Dividir componentes x,y por z | register \_ register |
| \_db                      | Dividir componentes x,y por z | register \_ db |
| \_Dw                      | Dividir componentes x,y por w | register \_ dw |
| \_da                      | Dividir componentes x,y por w | register \_ da |



 

### <a name="remarks"></a>Comentarios

El \_ modificador abstracto \_ o db hace lo siguiente:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



El \_ modificador dw o da hace lo \_ siguiente:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




