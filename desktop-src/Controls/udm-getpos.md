---
title: UDM_GETPOS mensaje (Commctrl.h)
description: Recupera la posición actual de un control hacia abajo con una precisión de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165506"
---
# <a name="udm_getpos-message"></a>Mensaje \_ GETPOS de UDM

Recupera la posición actual de un control hacia abajo con una precisión de 16 bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza [**correctamente, hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) se establece en cero y [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) se establece en la posición actual del control. Si se produce un error, **HIWORD** se establece en un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Al procesar este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana del compañero. El control de arriba a abajo devuelve un error si no hay ninguna ventana de compañeros o si el título especifica un valor no válido o fuera del intervalo. Además, se establece una marca de error en el HIWORD de la devolución si el control se crea sin el estilo [**\_ SETBUDDYINT de UDS,**](up-down-control-styles.md) aunque devuelve un valor de posición válido en el LOWORD de la devolución.

Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32,**](udm-setrange32.md)este mensaje devuelve solo los 16 bits inferiores de la posición. Para recuperar la posición completa de 32 bits, use [**UDM \_ GETPOS32**](udm-getpos32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

