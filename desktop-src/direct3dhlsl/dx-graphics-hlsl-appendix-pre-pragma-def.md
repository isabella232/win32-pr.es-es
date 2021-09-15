---
title: def pragma (directiva)
description: Directiva Pragma que asigna manualmente un registro de sombreador de punto flotante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- directiva pragma HLSL def
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568388"
---
# <a name="def-pragma-directive"></a>def pragma (directiva)

Directiva Pragma que asigna manualmente un registro de sombreador de punto flotante.



| \#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                        | Descripción                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*Objetivo*<br/>       | Destino que contiene el registro que se asignará. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*Registro*<br/> | Registro del sombreador de punto flotante que se asignará. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Primer byte del valor que se asignará al registro especificado. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Segundo byte del valor que se asignará al registro especificado. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Tercer byte del valor que se asignará al registro especificado. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Cuarto byte del valor que se asignará al registro especificado. <br/> |



 

## <a name="remarks"></a>Observaciones

La pragma def permite a un desarrollador rellenar previamente un registro de sombreador de punto flotante con el valor especificado. Esta pragma se usa con poca frecuencia.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Directiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





