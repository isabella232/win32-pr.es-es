---
title: EM_SETCTFOPENSTATUS mensaje (Richedit.h)
description: Abre o cierra el teclado Text Services Framework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062118"
---
# <a name="em_setctfopenstatus-message"></a>Mensaje \_ EM SETCTFOPENSTATUS

Abre o cierra el teclado Text Services Framework (TSF).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Para activar el teclado TSF, use **TRUE.** Para desactivar el teclado TSF, use **FALSE**.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este mensaje devuelve **TRUE.** Si no se realiza correctamente, este mensaje devuelve **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 





