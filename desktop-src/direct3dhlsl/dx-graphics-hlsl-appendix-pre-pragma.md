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
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568380"
---
# <a name="pragma-directive"></a>\#pragma (directiva)

Directiva de preprocesador que proporciona características específicas del equipo o específicas del sistema operativo, al tiempo que conserva la compatibilidad general con los lenguajes C y C++.



| \#pragma *token-string* |
|-------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Serie de caracteres que proporciona una instrucción y argumentos del compilador específicos. Este parámetro está sujeto a la expansión de macros. <br/> |



 

## <a name="remarks"></a>Observaciones

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

 

 





