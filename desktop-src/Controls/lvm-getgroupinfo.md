---
title: LVM_GETGROUPINFO mensaje (Commctrl.h)
description: Obtiene información de grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411399"
---
# <a name="lvm_getgroupinfo-message"></a>Mensaje GETGROUPINFO de LVM \_

Obtiene información de grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador que especifica el grupo cuya información se recupera.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**estructura LVGROUP**</a> que recibe la información recuperada. Establezca el **miembro cbSize** de esta estructura en sizeof(LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del grupo si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

Antes de intentar recuperar el encabezado de un grupo, asegúrese primero de que el grupo no tiene el estilo \_ LBGS NOHEADER.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





