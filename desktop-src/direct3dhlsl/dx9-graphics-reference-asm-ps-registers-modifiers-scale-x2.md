---
title: Escala del registro de origen x 2
description: Multiplique el valor por dos antes de usarlo en la instrucción.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983742"
---
# <a name="source-register-scale-x-2"></a>Escala del registro de origen x 2

Multiplique el valor por dos antes de usarlo en la instrucción.

## <a name="syntax"></a>Sintaxis


```
register_x2
```



## <a name="register"></a>Registrarse

Registro de origen. Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador se aplica solo a los datos leídos del registro.

Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.

Este modificador solo está disponible para las instrucciones aritméticas de la versión \_ 4.

## <a name="example"></a>Ejemplo

En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de-1 a + 1 y se calcula un producto de punto.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




