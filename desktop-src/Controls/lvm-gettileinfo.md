---
title: Mensaje de LVM_GETTILEINFO (commctrl. h)
description: Recupera información sobre un icono en un control de vista de lista.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079651"
---
# <a name="lvm_gettileinfo-message"></a>\_Mensaje GETTILEINFO LVM

Recupera información sobre un icono en un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que recibe la información recuperada.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

La vista en mosaico es una nueva forma de organizar y mostrar elementos en un control de vista de lista. Las demás vistas son el icono, el icono pequeño, los detalles y la lista.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





