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
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360798"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>ps \_ 1 \_ 4 source register modifiers for texld, texcrd

Las instrucciones de dirección de textura de la versión 1 4 del sombreador de dos \_ píxeles, [regld - ps \_ 1 \_ 4](texld---ps-1-4.md) y [texcrd - ps](texcrd---ps.md), tienen sintaxis personalizada. Estas instrucciones admiten su propio conjunto de modificadores de registro de origen, selectores de registro de origen y máscaras de escritura de registro de destino, como se muestra aquí.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificadores de registro de origen para regld y texcrd

Estos modificadores proporcionan funcionalidad de división projective dividiendo los valores x e y por los valores z o w.



| Modificadores de registro de origen | Descripción                | Sintaxis       |
|---------------------------|----------------------------|--------------|
| \_Dz                      | Dividir componentes x,y por z | register \_ register |
| \_db                      | Dividir componentes x,y por z | register \_ db |
| \_Dw                      | Dividir componentes x,y por w | register \_ dw |
| \_da                      | Dividir componentes x,y por w | register \_ da |



 

### <a name="remarks"></a>Observaciones

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

 

 




