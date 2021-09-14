---
title: TBM_CLEARSEL mensaje (Commctrl.h)
description: Borra el intervalo de selección actual en una barra de seguimiento.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166538"
---
# <a name="tbm_clearsel-message"></a>Mensaje \_ CLEARSEL de TBM

Borra el intervalo de selección actual en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE**, la barra de seguimiento se vuelve a dibujar después de borrar la selección.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una barra de seguimiento solo puede tener un intervalo de selección si especificó el estilo [**\_ ENABLESELRANGE**](trackbar-control-styles.md) de TBS cuando lo creó.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





