---
title: Mensaje de LVM_SETTILEINFO (commctrl. h)
description: Establece la información de un icono existente de un control de vista de lista.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- LVM_SETTILEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150130"
---
# <a name="lvm_settileinfo-message"></a>\_Mensaje SETTILEINFO LVM

Establece la información de un icono existente de un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que contiene la información que se va a establecer.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

**LVM \_ SETTILEINFO** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





