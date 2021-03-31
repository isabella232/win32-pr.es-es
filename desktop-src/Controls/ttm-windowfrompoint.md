---
title: Mensaje de TTM_WINDOWFROMPOINT (commctrl. h)
description: Permite que un procedimiento de subclase provoque que una información sobre herramientas muestre texto para una ventana distinta de la que se encuentra debajo del cursor del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802845"
---
# <a name="ttm_windowfrompoint-message"></a>TTM \_ WINDOWFROMPOINT

Permite que un procedimiento de subclase provoque que una información sobre herramientas muestre texto para una ventana distinta de la que se encuentra debajo del cursor del mouse.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que define el punto que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de la ventana que contiene el punto o **null** si no existe ninguna ventana en el punto especificado.

## <a name="remarks"></a>Observaciones

Este mensaje está diseñado para ser procesado por una aplicación que subclase una información sobre herramientas. No está diseñado para ser enviado por una aplicación. La información sobre herramientas envía este mensaje a sí mismo antes de mostrar el texto de una ventana. Al cambiar las coordenadas del punto especificado por *lParam*, el procedimiento de subclase puede hacer que la información sobre herramientas muestre texto para una ventana que no sea la que se encuentra debajo del cursor del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

