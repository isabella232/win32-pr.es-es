---
title: LVM_ISGROUPVIEWENABLED mensaje (Commctrl.h)
description: Comprueba si el control list-view tiene habilitada la vista de grupo.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- LVM_ISGROUPVIEWENABLED controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4934eb8f4b8dea9f31f589aab5e60798b83446cf0379ac7efbd4f1e67f5bef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079895"
---
# <a name="lvm_isgroupviewenabled-message"></a>Mensaje \_ DE LVM ISGROUPVIEWENABLED

Comprueba si el control list-view tiene habilitada la vista de grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** la vista de grupo está habilitada o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





