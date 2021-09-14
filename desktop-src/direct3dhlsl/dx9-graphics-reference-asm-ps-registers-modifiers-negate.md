---
title: Negate del registro de origen
description: Realiza un negate (y -x) en todos los componentes de registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360800"
---
# <a name="source-register-negate"></a>Negate del registro de origen

Realiza un negate (y = -x), en todos los componentes de registro.

## <a name="syntax"></a>Sintaxis


```
- register
```



## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

No se cambia el contenido del registro. El modificador solo se aplica a los datos leídos del registro. La operación de negación se aplica a los cuatro canales de color (RGBA).

Esta operación se realiza después de cualquier otro modificador presente en el mismo argumento.

Este modificador es mutuamente excluyente con [Source Register Invert,](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) por lo que no se puede aplicar al mismo registro.

Este modificador solo se usa con instrucciones aritméticas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar este modificador .


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




