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
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061840"
---
# <a name="lvm_getgroupinfo-message"></a>Mensaje \_ GETGROUPINFO de LVM

Obtiene información de grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador que especifica el grupo cuya información se recupera.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**estructura LVGROUP**</a> que recibe la información recuperada. Establezca el **miembro cbSize** de esta estructura en sizeof(LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del grupo si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de intentar recuperar el encabezado de un grupo, primero asegúrese de que el grupo no tiene el estilo \_ LBGS NOHEADER.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





