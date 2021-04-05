---
title: Mensaje de LVM_GETGROUPINFO (commctrl. h)
description: Obtiene la información del grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079205"
---
# <a name="lvm_getgroupinfo-message"></a>\_Mensaje GETGROUPINFO LVM

Obtiene la información del grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>IDENTIFICADOR que especifica el grupo cuya información se recupera.</dd> <dt>

*lParam* 
</dt> <dd>Puntero A una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que recibe la información recuperada. Establezca el miembro **cbSize** de esta estructura en SIZEOF (LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del grupo si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Antes de intentar recuperar el encabezado de un grupo, asegúrese primero de que el grupo no tenga el \_ estilo NOheader LBGS.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





