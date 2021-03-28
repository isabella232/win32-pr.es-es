---
title: Directiva pragma Def
description: Directiva pragma que asigna manualmente un registro de sombreador de punto flotante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Directiva pragma Def
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996824"
---
# <a name="def-pragma-directive"></a>Directiva pragma Def

Directiva pragma que asigna manualmente un registro de sombreador de punto flotante.



| \#pragma DEF ( *destino*, *registro*, *val1*, *val2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                        | Descripción                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*dirigir*<br/>       | Destino que contiene el registro que se va a asignar. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*el*<br/> | Registro del sombreador de punto flotante que se va a asignar. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Primer byte del valor que se va a asignar al registro especificado. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*valor1*<br/>             | Segundo byte del valor que se va a asignar al registro especificado. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Tercer byte del valor que se va a asignar al registro especificado. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Cuarto byte del valor que se va a asignar al registro especificado. <br/> |



 

## <a name="remarks"></a>Observaciones

La pragma Def permite a un desarrollador rellenar previamente un registro de sombreador de punto flotante con el valor especificado. Esta pragma se usa con poca frecuencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





