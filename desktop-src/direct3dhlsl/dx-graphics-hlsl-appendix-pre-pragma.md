---
title: " pragma (directiva)"
description: Directiva de preprocesador que proporciona características específicas del equipo o específicas del sistema operativo, al tiempo que conserva la compatibilidad general con los lenguajes C y C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Directiva pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024615"
---
# <a name="pragma-directive"></a>\#pragma (directiva)

Directiva de preprocesador que proporciona características específicas del equipo o específicas del sistema operativo, al tiempo que conserva la compatibilidad general con los lenguajes C y C++.



| \#pragma *token-string* |
|-------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Serie de caracteres que proporciona una instrucción y argumentos del compilador específicos. Este parámetro está sujeto a la expansión de macros. <br/> |



 

## <a name="remarks"></a>Comentarios

Si el compilador encuentra una pragma que no reconoce, emite una advertencia, pero la compilación continúa.

El compilador HLSL reconoce las siguientes pragmas:

-   [Def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [Matriz de \_ paquetes](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





