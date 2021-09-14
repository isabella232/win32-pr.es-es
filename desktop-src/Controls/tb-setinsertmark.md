---
title: TB_SETINSERTMARK mensaje (Commctrl.h)
description: Establece la marca de inserción actual de la barra de herramientas.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166602"
---
# <a name="tb_setinsertmark-message"></a>Mensaje \_ DE TB SETINSERTMARK

Establece la marca de inserción actual de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que contiene la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ GETINSERTMARK**](tb-getinsertmark.md)
</dt> </dl>

 

 





