---
title: Mensaje de LVM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- LVM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b1e29d933892a24d7bc2ab472c7d591375362a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658328"
---
# <a name="lvm_setunicodeformat-message"></a>\_Mensaje SETUNICODEFORMAT LVM

Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetUnicodeFormat de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina el juego de caracteres utilizado por el control. Si este valor es distinto de cero, el control usará caracteres Unicode. Si este valor es cero, el control usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode anterior para el control.

## <a name="remarks"></a>Observaciones

Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETUNICODEFORMAT LVM**](lvm-getunicodeformat.md)
</dt> </dl>

 

 





