---
title: TBM_GETTHUMBRECT mensaje (Commctrl.h)
description: Recupera el tamaño y la posición del rectángulo delimitador para el control deslizante en una barra de seguimiento.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166486"
---
# <a name="tbm_getthumbrect-message"></a>Mensaje \_ GETTHUMBRECT de TBM

Recupera el tamaño y la posición del rectángulo delimitador para el control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) El mensaje rellena esta estructura con el rectángulo delimitador del control deslizante de la barra de seguimiento en coordenadas de cliente de la ventana de la barra de seguimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

