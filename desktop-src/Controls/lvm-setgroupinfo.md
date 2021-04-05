---
title: Mensaje de LVM_SETGROUPINFO (commctrl. h)
description: Establece la información del grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078862"
---
# <a name="lvm_setgroupinfo-message"></a>\_Mensaje SETGROUPINFO LVM

Establece la información del grupo. Envíe este mensaje explícitamente o mediante la [**macro \_ SetGroupInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>IDENTIFICADOR que especifica el grupo cuya información se va a establecer.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntero a una estructura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contiene la información que se va a establecer.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del grupo si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Para cambiar el identificador de un grupo existente, agregue <b>LVGF_GROUPID</b> a <b>LVGROUP. Mask</b> y establezca <b>LVGROUP. iGroupId</b> en el nuevo identificador. Se producirá un error en la llamada si <b>LVGROUP. iGroupId</b> contiene el identificador de un grupo existente.

Para actualizar otras propiedades de un grupo existente (por ejemplo, actualizar una alineación del texto del encabezado o del pie de página del grupo, <b>uAlign</b>) <b>LVGROUP. Mask</b> no debe contener <b>LVGF_GROUPID</b>. de lo contrario, se producirá un error en la actualización.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





