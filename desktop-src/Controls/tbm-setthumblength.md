---
title: TBM_SETTHUMBLENGTH mensaje (Commctrl.h)
description: Establece la longitud del control deslizante en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el estilo \_ FIXEDLENGTH de TBS.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166418"
---
# <a name="tbm_setthumblength-message"></a>Mensaje \_ TBM SETTHUMBLENGTH

Establece la longitud del control deslizante en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**estilo \_ FIXEDLENGTH de TBS.**](trackbar-control-styles.md)

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)
</dt> </dl>

 

 





