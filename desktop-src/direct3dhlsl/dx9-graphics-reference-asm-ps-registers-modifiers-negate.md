---
title: Registro de origen negativo
description: Realiza una negación (y-x) en todos los componentes del registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075612"
---
# <a name="source-register-negate"></a>Registro de origen negativo

Realiza una negación (y =-x) en todos los componentes del registro.

## <a name="syntax"></a>Sintaxis


```
- register
```



## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador se aplica solo a los datos leídos del registro. La operación de negación se aplica a los cuatro canales de color (RGBA).

Esta operación se realiza después de cualquier otro modificador presente en el mismo argumento.

Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , por lo que no se puede aplicar al mismo registro.

Este modificador solo se usa con instrucciones aritméticas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo utilizar este modificador.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




