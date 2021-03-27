---
title: Desviación del registro de origen
description: Reste 0,5 de todos los componentes.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994599"
---
# <a name="source-register-bias"></a>Desviación del registro de origen

Reste 0,5 de todos los componentes.

## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, vea [PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador se aplica solo a los datos leídos del registro. La diferencia se aplica a los cuatro canales de color (RGBA) de la siguiente manera:


```
output = (input - 0.5)
```



El efecto es modificar los datos que estaban en el intervalo de 0 a 1 para que estén en el intervalo de-0,5 a 0,5. Aplicar el sesgo a los datos que están fuera de este intervalo puede producir resultados indefinidos.

> [!Note]  
> Este modificador es mutuamente excluyente con la [inversión del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.

 

Este modificador es para su uso con las instrucciones aritméticas.

## <a name="example"></a>Ejemplo

Este ejemplo realiza la misma operación que D3DTOP \_ ADDSIGNED en la sintaxis de varias texturas de DirectX 6,0 y 7,0.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




