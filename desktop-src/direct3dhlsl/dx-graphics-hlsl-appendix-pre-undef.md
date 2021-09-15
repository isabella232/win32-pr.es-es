---
title: " undef (Directiva)"
description: Directiva de preprocesador que quita la definición actual de una constante o macro que se definió previamente mediante la directiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- directiva undef HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568376"
---
# <a name="undef-directive"></a>\#undef (Directiva)

Directiva de preprocesador que quita la definición actual de una constante o macro que se definió previamente mediante la [ \# directiva define.](dx-graphics-hlsl-appendix-pre-define.md)



| \#identificador *undef* |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                              | Descripción                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/> | Identificador de la constante o macro de la que se quitará la definición. Si no está delimitando una macro, proporcione solo el identificador, no la lista de parámetros. <br/> |



 

## <a name="remarks"></a>Observaciones

Puede aplicar la directiva undef a un identificador que no tenga ninguna definición anterior; esto garantiza que \# el identificador no está definido. El reemplazo de macro no se realiza dentro \# de instrucciones undef.

La directiva undef normalmente se empareja con una directiva define para crear una región en un programa de origen en el que un identificador \# tiene un significado especial. [ \# ](dx-graphics-hlsl-appendix-pre-define.md) Por ejemplo, una función específica del programa de origen puede utilizar constantes de manifiesto para definir valores específicos del entorno que no afecten al resto del programa. La \# directiva undef también funciona con la directiva [) para controlar la compilación condicional del programa de origen.

Las constantes y macros pueden no definirse desde la línea de comandos mediante la opción /U, seguidas de los identificadores que se deben no definir. Esto equivale a agregar una secuencia de \# directivas undef al principio del archivo de origen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar \# la directiva undef para quitar definiciones de una constante simbólica y una macro.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define (Directiva, HLSL de DirectX)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#if, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





