---
title: Mensaje de EM_SCROLLCARET (Winuser. h)
description: Desplaza el símbolo de intercalación en la vista de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151147"
---
# <a name="em_scrollcaret-message"></a>\_Mensaje SCROLLCARET em

Desplaza el símbolo de intercalación en la vista de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro está reservado. Debe establecerse en cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro está reservado. Debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto no es significativo.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_LINESCROLL em**](em-linescroll.md)
</dt> <dt>

[**\_desplazar em**](em-scroll.md)
</dt> <dt>

[**VSCROLL de WM \_**](wm-vscroll.md)
</dt> </dl>

 

 





