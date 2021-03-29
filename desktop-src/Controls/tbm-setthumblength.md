---
title: Mensaje de TBM_SETTHUMBLENGTH (commctrl. h)
description: Establece la longitud del control deslizante en una barra de desplazamiento. Este mensaje se omite si TrackBar no tiene el \_ estilo FIXEDLENGTH de TBS.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535127"
---
# <a name="tbm_setthumblength-message"></a>TBM \_ SETTHUMBLENGTH

Establece la longitud del control deslizante en una barra de desplazamiento. Este mensaje se omite si TrackBar no tiene el estilo [**\_ FIXEDLENGTH de TBS**](trackbar-control-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Longitud, en píxeles, del control deslizante.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

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

[**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)
</dt> </dl>

 

 





