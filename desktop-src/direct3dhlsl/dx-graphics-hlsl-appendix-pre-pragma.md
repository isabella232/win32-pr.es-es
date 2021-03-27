---
title: " pragma (Directiva)"
description: Directiva de preprocesador que proporciona características específicas del equipo o del sistema operativo, a la vez que conserva la compatibilidad total con los lenguajes C y C++.
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076746"
---
# <a name="pragma-directive"></a>\#pragma (Directiva)

Directiva de preprocesador que proporciona características específicas del equipo o del sistema operativo, a la vez que conserva la compatibilidad total con los lenguajes C y C++.



| \#*cadena de token de* pragma |
|-------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*<br/> | Serie de caracteres que proporciona una instrucción de compilador y argumentos concretos. Este parámetro está sujeto a la expansión de macros. <br/> |



 

## <a name="remarks"></a>Observaciones

Si el compilador encuentra una directiva pragma que no reconoce, emite una advertencia, pero la compilación continúa.

El compilador de HLSL reconoce las siguientes pragmas:

-   [Def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [matriz de paquetes \_](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





