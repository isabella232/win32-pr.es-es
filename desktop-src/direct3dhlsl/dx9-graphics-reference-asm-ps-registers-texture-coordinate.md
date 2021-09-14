---
title: Registro de coordenadas de textura (referencia de HLSL PS)
description: Registro de entrada del sombreador de píxeles que contiene coordenadas de textura.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263916"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Registro de coordenadas de textura (referencia de HLSL PS)

Registro de entrada del sombreador de píxeles que contiene coordenadas de textura.



| Versiones del sombreador de píxeles       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura |      |      |      |      | x    | x     | x    | x    | x     |



 

Un registro de coordenadas de textura contiene datos de coordenadas de textura. Antes de usar un registro de coordenadas de textura, debe declararse mediante una declaración de sombreador de píxeles. Para obtener más información sobre cómo declarar un registro de textura, [vea dcl - (sm2, sm3 - ps asm).](dcl---ps.md)

Además, estas son algunas otras propiedades de los registros de coordenadas de textura.

-   Hay ocho registros de coordenadas de textura de sombreador de píxeles, de t0 a t7.
-   Se trata de registros de solo lectura.
-   Contienen valores RGBA de cuatro componentes iterados a partir de los vértices de entrada.
-   Contienen valores de datos de intervalo dinámico alto y de alta precisión interpolados a partir de los datos de vértice. Los valores se generan con interpolación con perspectiva correcta. Los datos son de precisión de punto flotante y están firmados.
-   Hay un máximo de uno en una sola instrucción.
-   Varias lecturas de un registro de coordenadas de textura dentro de un sombreador deben usar una [máscara de escritura de registro de destino idéntica.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)
-   El modificador de precisión parcial \[ \_ opcional pp se aplica a \] las lecturas dependientes. Esto se debe a que la precisión parcial afecta a las operaciones aritméticas que implican el registro de coordenadas de textura. No afectará a la precisión de las instrucciones de dirección de textura porque no afecta a los iteradores de coordenadas de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




