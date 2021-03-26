---
title: Inversión del registro de origen
description: Realiza un cálculo de (1 valor) para cada canal del registro especificado.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983743"
---
# <a name="source-register-invert"></a>Inversión del registro de origen

Realiza un cálculo de (1 valor) para cada canal del registro especificado.

## <a name="syntax"></a>Sintaxis


```
1 - register
```



## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador se aplica solo a los datos leídos del registro. La operación de inversión se aplica a los cuatro canales de color (RGBA).

Este modificador solo se puede usar con instrucciones aritméticas. Además, este modificador no se puede combinar con la otra [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Ejemplo

En este ejemplo se usa inversion para generar el complemento del registro R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




