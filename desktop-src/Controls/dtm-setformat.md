---
title: DTM_SETFORMAT mensaje (Commctrl.h)
description: Establece la presentación de un control selector de fecha y hora (DTP) basado en una cadena de formato determinada. Puede enviar este mensaje explícitamente o usar la macro DateTime \_ SetFormat.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273351"
---
# <a name="dtm_setformat-message"></a>Mensaje \_ SETFORMAT de DTM

Establece la presentación de un control selector de fecha y hora (DTP) basado en una cadena de formato determinada. Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena de formato terminada [en cero](date-and-time-picker-controls.md) que define la presentación deseada. Si se establece este parámetro **en NULL,** se restablecerá el control a la cadena de formato predeterminada para el estilo actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Es aceptable incluir caracteres adicionales dentro de la cadena de formato para generar una presentación más completa. Sin embargo, los caracteres sin formato deben incluirse entre comillas simples. Por ejemplo, la cadena de formato "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" produciría una salida como "Today is: 04:22:31 Tuesday Mar 23, 1996".

> [!Note]  
> Un control DTP realiza un seguimiento de los cambios de configuración regional cuando usa la cadena de formato predeterminada. Si establece una cadena de formato personalizado, no se actualizará en respuesta a los cambios de configuración regional.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) y **DTM \_ SETFORMATA** (ANSI)<br/>               |



 

 





