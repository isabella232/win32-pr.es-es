---
title: Escala de registro de origen x 2
description: Multiplique el valor por dos antes de usarlo en la instrucción .
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc07605d0b570ce9647a8091d9eef7f7a6ad4ecaaeee96ce2d04aaaa3d8bcdd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024175"
---
# <a name="source-register-scale-x-2"></a>Escala de registro de origen x 2

Multiplique el valor por dos antes de usarlo en la instrucción .

## <a name="syntax"></a>Syntax


```
register_x2
```



## <a name="register"></a>Registrarse

Registro de origen. Para obtener más información sobre los tipos de registro, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentarios

No se cambia el contenido del registro. El modificador solo se aplica a los datos leídos del registro.

Este modificador es mutuamente excluyente con [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.

Este modificador solo está disponible para las instrucciones aritméticas de la versión 1 \_ 4.

## <a name="example"></a>Ejemplo

En este ejemplo se muestrea una textura, se convierten los datos en el intervalo de -1 a +1 y se calcula un producto de punto.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




