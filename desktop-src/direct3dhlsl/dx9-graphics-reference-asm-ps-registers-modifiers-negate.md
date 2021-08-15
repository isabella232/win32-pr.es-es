---
title: Source Register Negate
description: Realiza un negate (y -x) en todos los componentes de registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94898dbbf193254165850ee696d2fea72d6d446908021dfbb5fd32f1920b7010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512956"
---
# <a name="source-register-negate"></a>Source Register Negate

Realiza un negate (y = -x) en todos los componentes de registro.

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>Registros

Registro de origen. Para obtener más información sobre los tipos de registro, [vea ps \_ \_ 1 \_ \_ 1 ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentarios

No se cambia el contenido del registro. El modificador solo se aplica a los datos leídos del registro. La operación de negación se aplica a los cuatro canales de color (RGBA).

Esta operación se realiza después de cualquier otro modificador presente en el mismo argumento.

Este modificador es mutuamente excluyente con [Source Register Invert,](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) por lo que no se puede aplicar al mismo registro.

Este modificador solo se usa con instrucciones aritméticas.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar este modificador.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




