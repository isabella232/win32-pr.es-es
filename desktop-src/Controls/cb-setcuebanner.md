---
title: CB_SETCUEBANNER mensaje (Winuser.h)
description: Establece el texto del banner de la indicación que se muestra para el control de edición de un cuadro combinado.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER controles de Windows mensaje
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
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089045"
---
# <a name="cb_setcuebanner-message"></a>Mensaje \_ DE CB SETCUEBANNER

Establece el texto del banner de la indicación que se muestra para el control de edición de un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer de cadena Unicode terminada en NULL que contiene el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente o, de lo contrario, devuelve un valor de error.

## <a name="remarks"></a>Comentarios

El banner de indicación es texto que se muestra en el control de edición de un cuadro combinado cuando no hay ninguna selección.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





