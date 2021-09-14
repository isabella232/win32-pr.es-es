---
title: LVM_HASGROUP mensaje (Commctrl.h)
description: Determina si el control list-view tiene un grupo especificado.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061810"
---
# <a name="lvm_hasgroup-message"></a>Mensaje \_ HASGROUP de LVM

Determina si el control list-view tiene un grupo especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador del grupo.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser **NULL.**</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el control list-view tiene el grupo especificado o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





