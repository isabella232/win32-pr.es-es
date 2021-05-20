---
title: message pragma (Directiva)
description: Directiva Pragma que genera mensajes en tiempo de compilador.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- message pragma Directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153488"
---
# <a name="message-pragma-directive"></a>message pragma (Directiva)

Directiva Pragma que genera mensajes en tiempo de compilador.



| \#pragma message("*token-string*") |
|-----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                    | Descripción                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Mensaje del compilador.<br/> |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el procesamiento de mensajes durante el preprocesamiento.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Directiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





