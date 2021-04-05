---
title: Mensaje de TBM_SETSELSTART (commctrl. h)
description: Establece la posición lógica inicial del intervalo de selección actual en una barra de inicio. Este mensaje se omite si TrackBar no tiene el \_ estilo ENABLESELRANGE de TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078851"
---
# <a name="tbm_setselstart-message"></a>TBM \_ SETSELSTART

Establece la posición lógica inicial del intervalo de selección actual en una barra de inicio. Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar el marcador. Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar después de establecer el intervalo de selección. Si este parámetro es **false**, el mensaje establece el intervalo de selección, pero no vuelve a dibujar el TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición inicial del intervalo de selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





