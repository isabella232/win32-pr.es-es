---
title: Mensaje de CB_SETCUEBANNER (Winuser. h)
description: Establece el texto del titular de indicación que se muestra para el control de edición de un cuadro combinado.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079358"
---
# <a name="cb_setcuebanner-message"></a>\_Mensaje SETCUEBANNER CB

Establece el texto del titular de indicación que se muestra para el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un búfer de cadena Unicode terminada en null que contiene el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente, o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

El banner de indicación es el texto que se muestra en el control de edición de un cuadro combinado cuando no hay ninguna selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





