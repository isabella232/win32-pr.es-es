---
title: '\_ \_ modificadores de registro de origen de PS 1 4 para texld, texcrd'
description: Dos \_ instrucciones de dirección de textura del sombreador de píxeles versión 1 4, texld-PS \_ 1 \_ 4 y texcrd-PS, tienen una sintaxis personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104149023"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>\_ \_ modificadores de registro de origen de PS 1 4 para texld, texcrd

Dos \_ instrucciones de dirección de textura del sombreador de píxeles versión 1 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) y [texcrd-PS](texcrd---ps.md), tienen una sintaxis personalizada. Estas instrucciones admiten su propio conjunto de modificadores de registro de origen, selectores de registro de origen y máscaras de escritura de registro de destino, como se muestra aquí.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificadores de registro de origen para texld y texcrd

Estos modificadores proporcionan funcionalidad de división proyectada dividiendo los valores x e y por los valores z o w.



| Modificadores de registro de origen | Descripción                | Sintaxis       |
|---------------------------|----------------------------|--------------|
| \_DZ                      | Dividir componentes x, y por z | registrar \_ DZ |
| \_db                      | Dividir componentes x, y por z | registrar \_ base de registros |
| \_almacenamiento                      | Dividir componentes x, y en w | registrar \_ DW |
| \_da                      | Dividir componentes x, y en w | registrar \_ da |



 

### <a name="remarks"></a>Observaciones

El \_ \_ modificador DZ o DB hace lo siguiente:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



El \_ \_ modificador DW o da hace lo siguiente:


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

 

 




