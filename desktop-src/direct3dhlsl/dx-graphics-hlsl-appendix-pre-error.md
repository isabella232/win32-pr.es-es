---
title: " error (Directiva)"
description: Directiva de preprocesador que genera mensajes de error en tiempo de compilación.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- HLSL de la Directiva de error
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419546"
---
# <a name="error-directive"></a>\#error (Directiva)

Directiva de preprocesador que genera mensajes de error en tiempo de compilación.



| \#*token de error: cadena* |
|------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*<br/> | Mensaje de error. Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas. La cadena de token está sujeta a la expansión de macros. <br/> |



 

## <a name="remarks"></a>Observaciones

\#las directivas de error son más útiles para detectar incoherencias del programador e infracciones de las restricciones durante el preprocesamiento. Cuando \# se encuentra una directiva de error, la compilación finaliza.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el procesamiento de errores durante el preprocesamiento.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





