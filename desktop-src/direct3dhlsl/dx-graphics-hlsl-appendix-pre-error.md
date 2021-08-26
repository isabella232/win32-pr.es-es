---
title: " error (directiva)"
description: Directiva de preprocesador que genera mensajes de error en tiempo del compilador.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- directiva HLSL de error
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fa1af02a693b5168a2d96e653726fd0a468587bf2b8c1825afbf8e73057f61f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068335"
---
# <a name="error-directive"></a>\#error (directiva)

Directiva de preprocesador que genera mensajes de error en tiempo del compilador.



| \#error *token-string* |
|------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Mensaje de error. Este parámetro consta de una serie de tokens, como palabras clave, constantes o instrucciones completas. La cadena de token está sujeta a la expansión de macros. <br/> |



 

## <a name="remarks"></a>Comentarios

\#Las directivas de error son más útiles para detectar incoherencias del programador y la infracción de restricciones durante el preprocesamiento. Cuando se \# encuentra una directiva de error, la compilación finaliza.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el procesamiento de errores durante el preprocesamiento.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





