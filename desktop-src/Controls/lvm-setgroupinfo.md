---
title: LVM_SETGROUPINFO mensaje (Commctrl.h)
description: Establece la información de grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974067"
---
# <a name="lvm_setgroupinfo-message"></a>Mensaje \_ SETGROUPINFO de LVM

Establece la información de grupo. Envíe este mensaje explícitamente o mediante la macro [**\_ SetGroupInfo de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>Identificador que especifica el grupo cuya información se va a establecer.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntero a una [**estructura LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contiene la información que se debe establecer.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del grupo si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Observaciones

Para cambiar un identificador de grupo de un grupo existente, agregue <b>LVGF_GROUPID</b> a <b>LVGROUP.mask</b> y establezca <b>LVGROUP.iGroupId</b> en el nuevo identificador. Se producirá un error en <b>la llamada si LVGROUP.iGroupId</b> contiene el identificador de un grupo existente.

Para actualizar otras propiedades de un grupo existente (por ejemplo, actualizar una alineación del texto de encabezado o pie de página para el grupo, <b>uAlign</b>) <b>LVGROUP.mask</b> no debe contener LVGF_GROUPID ; <b>de</b>lo contrario, se producirá un error en la actualización.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





