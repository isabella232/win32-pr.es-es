---
title: TB_GETINSERTMARK mensaje (Commctrl.h)
description: Recupera la marca de inserción actual de la barra de herramientas.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ee4a51d3110a99013ed26ccb1f2c102e7821873e63dd419b33e92636a1b655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918755"
---
# <a name="tb_getinsertmark-message"></a>Mensaje \_ DE TB GETINSERTMARK

Recupera la marca de inserción actual de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recibe la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





