---
title: Mensaje de UDM_GETPOS (commctrl. h)
description: Recupera la posición actual de un control de flechas con una precisión de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656483"
---
# <a name="udm_getpos-message"></a>\_Mensaje GETPOS UDM

Recupera la posición actual de un control de flechas con una precisión de 16 bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) se establece en cero y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) se establece en la posición actual del control. Si se produce un error, **HIWORD** se establece en un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Al procesar este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana relacionada. El control de flechas devuelve un error si no hay ninguna ventana relacionada o si el título especifica un valor que no es válido o está fuera del intervalo. Además, se establece una marca de error en el HIWORD de devolución si el control se crea sin el estilo [**uds \_ SETBUDDYINT**](up-down-control-styles.md) , aunque devuelva un valor de posición válido en el LOWORD de la devolución.

Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32**](udm-setrange32.md), este mensaje devuelve solo los 16 bits inferiores de la posición. Para recuperar la posición completa de 32 bits, use [**UDM \_ GETPOS32**](udm-getpos32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETRANGE32**](udm-getrange32.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETRANGE32**](udm-setrange32.md)
</dt> </dl>

 

