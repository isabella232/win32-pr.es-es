---
title: Mensaje de TBM_GETTHUMBRECT (commctrl. h)
description: Recupera el tamaño y la posición del rectángulo delimitador del control deslizante en una barra de desplazamiento.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079395"
---
# <a name="tbm_getthumbrect-message"></a>TBM \_ GETTHUMBRECT

Recupera el tamaño y la posición del rectángulo delimitador del control deslizante en una barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . El mensaje rellena esta estructura con el rectángulo delimitador del control deslizante de la barra de desplazamiento en las coordenadas de cliente de la ventana de la barra de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

