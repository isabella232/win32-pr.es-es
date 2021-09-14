---
title: TTM_WINDOWFROMPOINT mensaje (Commctrl.h)
description: Permite que un procedimiento de subclase haga que una información sobre herramientas muestre texto para una ventana que no sea la que hay debajo del cursor del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165818"
---
# <a name="ttm_windowfrompoint-message"></a>MENSAJE \_ DE VENTANA DE TTMFROMPOINT

Permite que un procedimiento de subclase haga que una información sobre herramientas muestre texto para una ventana que no sea la que hay debajo del cursor del mouse.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que define el punto que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de la ventana que contiene el punto o **NULL** si no existe ninguna ventana en el punto especificado.

## <a name="remarks"></a>Observaciones

Este mensaje está pensado para que lo procese una aplicación que subclases una información sobre herramientas. No está pensado para que lo envíe una aplicación. Una información sobre herramientas envía este mensaje a sí mismo antes de mostrar el texto de una ventana. Al cambiar las coordenadas del punto especificado por *lParam*, el procedimiento de subclase puede hacer que la información sobre herramientas muestre texto para una ventana que no sea la que hay debajo del cursor del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

