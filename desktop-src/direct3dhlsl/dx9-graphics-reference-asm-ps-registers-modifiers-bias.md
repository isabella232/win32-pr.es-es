---
title: Sesgo del registro de origen
description: Resta 0,5 de todos los componentes.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264012"
---
# <a name="source-register-bias"></a>Sesgo del registro de origen

Resta 0,5 de todos los componentes.

## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador solo se aplica a los datos leídos del registro. El sesgo se aplica a los cuatro canales de color (RGBA) de la siguiente manera:


```
output = (input - 0.5)
```



El efecto es modificar los datos que se encontraban en el intervalo de 0 a 1 para que se encontrara en el intervalo de -0,5 a 0,5. La aplicación de sesgos a datos fuera de este intervalo puede producir resultados indefinidos.

> [!Note]  
> Este modificador es mutuamente excluyente con [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), por lo que no se puede aplicar al mismo registro.

 

Este modificador se usa con las instrucciones aritméticas.

## <a name="example"></a>Ejemplo

En este ejemplo se realiza la misma operación que D3DTOP ADDSIGNED en la sintaxis de varias texturas de \_ DirectX 6.0 y 7.0.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




