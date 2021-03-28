---
title: Registro de coordenadas de textura (referencia de PS de HLSL)
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
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104983915"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Registro de coordenadas de textura (referencia de PS de HLSL)

Registro de entrada del sombreador de píxeles que contiene coordenadas de textura.



| Versiones del sombreador de píxeles       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura |      |      |      |      | x    | x     | x    | x    | x     |



 

Un registro de coordenadas de textura contiene datos de coordenadas de textura. Antes de utilizar un registro de coordenadas de textura, se debe declarar mediante una declaración de sombreador de píxeles. Para obtener más información sobre cómo declarar un registro de textura, consulte [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).

Además, estas son otras propiedades de los registros de coordenadas de textura.

-   Hay ocho registros de coordenadas de textura del sombreador de píxeles, T0 a T7.
-   Se trata de registros de solo lectura.
-   Contienen valores RGBA de cuatro componentes que se iteran desde los vértices de entrada.
-   Contienen valores de datos de rango dinámico alto y alta precisión interpolados a partir de los datos de vértices. Los valores se generan con la interpolación correcta de la perspectiva. Los datos son una precisión de punto flotante y están firmados.
-   Hay un máximo de uno en una sola instrucción.
-   Varias lecturas de un registro de coordenadas de textura dentro de un sombreador deben usar la misma [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   El modificador de precisión parcial opcional \[ \_ PP \] se aplica a las lecturas dependientes. Esto se debe a que la precisión parcial afecta a las operaciones aritméticas que implican el registro de coordenadas de textura. No afectará a la precisión de las instrucciones de dirección de textura, ya que no afecta a los iteradores de coordenadas de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




