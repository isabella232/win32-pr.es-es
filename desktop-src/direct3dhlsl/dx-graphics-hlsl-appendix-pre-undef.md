---
title: " UNDEF (Directiva)"
description: Directiva de preprocesador que quita la definición actual de una constante o macro que se definió anteriormente mediante la Directiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- UNDEF (Directiva HLSL)
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358111"
---
# <a name="undef-directive"></a>\#UNDEF (Directiva)

Directiva de preprocesador que quita la definición actual de una constante o macro que se definió anteriormente mediante la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .



| \#UNDEF ( *identificador* ) |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                              | Descripción                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*<br/> | Identificador de la constante o macro para la que se va a quitar la definición. Si va a desdefinir una macro, proporcione solo el identificador, no la lista de parámetros. <br/> |



 

## <a name="remarks"></a>Observaciones

Puede aplicar la \# Directiva UNDEF a un identificador que no tiene ninguna definición anterior; esto garantiza que el identificador no esté definido. La sustitución de macros no se realiza dentro de las \# instrucciones UNDEF.

\#Normalmente, la Directiva UNDEF se empareja con una directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para crear una región en un programa de origen en el que un identificador tiene un significado especial. Por ejemplo, una función específica del programa de origen puede utilizar constantes de manifiesto para definir valores específicos del entorno que no afecten al resto del programa. La \# Directiva UNDEF también funciona con la Directiva [) para controlar la compilación condicional del programa de origen.

Las constantes y macros pueden estar sin definir desde la línea de comandos mediante la opción/U, seguido de los identificadores para que no estén definidos. Esto es equivalente a agregar una secuencia de \# directivas UNDEF al principio del archivo de código fuente.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar la \# Directiva UNDEF para quitar definiciones de una constante simbólica y una macro.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Si,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





