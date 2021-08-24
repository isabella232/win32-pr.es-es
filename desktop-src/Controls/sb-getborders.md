---
title: SB_GETBORDERS mensaje (Commctrl.h)
description: Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafa7a8c27b5c274a981e43edc5c55ec0cade67cac08a1d09a898916d792795c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169058"
---
# <a name="sb_getborders-message"></a>Mensaje \_ SB GETBORDERS

Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que tiene tres elementos. El primer elemento recibe el ancho del borde horizontal, el segundo recibe el ancho del borde vertical y el tercero recibe el ancho del borde entre rectángulos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Los bordes determinan el espaciado entre el borde exterior de la ventana y los rectángulos dentro de la ventana que contienen texto. Los bordes también determinan el espaciado entre rectángulos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





