---
title: Message pragma (Directiva)
description: Directiva pragma que genera mensajes en tiempo de compilación.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Message pragma Directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784462"
---
# <a name="message-pragma-directive"></a>Message pragma (Directiva)

Directiva pragma que genera mensajes en tiempo de compilación.



| \#pragma Message "*token-String*" |
|-----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-cadena*<br/> | Mensaje del compilador.<br/> |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el procesamiento de mensajes durante el preprocesamiento.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





