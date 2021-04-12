---
title: Mensaje de UDM_GETPOS32 (commctrl. h)
description: Devuelve la posición de 32 bits de un control de flechas.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489617"
---
# <a name="udm_getpos32-message"></a>\_Mensaje GETPOS32 UDM

Devuelve la posición de 32 bits de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor **booleano** que se establece en cero si el valor se recupera correctamente o es distinto de cero si se produce un error. Si este parámetro se establece en **null**, no se registran los errores.

Si se usa **UDM \_ GETPOS32** en una situación entre procesos, este parámetro debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición de un control de flechas con una precisión de 32 bits. Las aplicaciones deben comprobar el valor *lParam* para determinar si el valor devuelto es válido.

## <a name="remarks"></a>Observaciones

Al procesar este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana relacionada. Devuelve un error si no hay ninguna ventana relacionada o si el título especifica un valor que no es válido o está fuera del intervalo.

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

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





