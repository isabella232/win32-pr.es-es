---
title: LVM_SETINSERTMARKCOLOR mensaje (Commctrl.h)
description: Establece el color del punto de inserción.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- LVM_SETINSERTMARKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135275faa83f16956cfdeab90aaddded93caf2127f57c395a83deb4b29dd442a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919845"
---
# <a name="lvm_setinsertmarkcolor-message"></a>Mensaje \_ LVM SETINSERTMARKCOLOR

Establece el color del punto de inserción.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>**Estructura COLORREF** que especifica el color para establecer el punto de inserción.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **la estructura COLORREF** establecida en el color anterior.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





