---
title: UDM_GETPOS32 mensaje (Commctrl.h)
description: Devuelve la posición de 32 bits de un control hacia abajo.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165505"
---
# <a name="udm_getpos32-message"></a>Mensaje \_ GETPOS32 de UDM

Devuelve la posición de 32 bits de un control hacia abajo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un **valor BOOL** que se establece en cero si el valor se recupera correctamente o es distinto de cero si se produce un error. Si este parámetro se establece en **NULL, no** se notifican los errores.

Si **se usa \_ UDM GETPOS32** en una situación entre procesos, este parámetro debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición de un control hacia abajo con una precisión de 32 bits. Las aplicaciones deben comprobar el *valor lParam* para determinar si el valor devuelto es válido.

## <a name="remarks"></a>Observaciones

Cuando procesa este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana de compañeros. Devuelve un error si no hay ninguna ventana de compañeros o si el título especifica un valor no válido o fuera del intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





