---
title: Mensaje de DTM_SETFORMAT (commctrl. h)
description: Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada. Puede enviar este mensaje explícitamente o utilizar la macro SetFormat de fecha y hora \_ .
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079573"
---
# <a name="dtm_setformat-message"></a>DTM \_ SETFORMAT

Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetFormat de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [cadena de formato](date-and-time-picker-controls.md) terminada en cero que define la presentación deseada. Si se establece este parámetro en **null** , se restablecerá el control en la cadena de formato predeterminada para el estilo actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Es aceptable incluir caracteres adicionales en la cadena de formato para generar una pantalla más enriquecida. Sin embargo, los caracteres que no sean de formato deben encerrarse entre comillas simples. Por ejemplo, la cadena de formato "' hoy es: ' HH ': ' m ': ddddMMMdd ', ' yyy" produciría una salida como "hoy es: 04:22:31 martes, 23, 1996".

> [!Note]  
> Un control de DTP realiza un seguimiento de los cambios de la configuración regional cuando se usa la cadena de formato predeterminada. Si establece una cadena de formato personalizado, no se actualizará en respuesta a los cambios de la configuración regional.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) y **DTM \_ SETFORMATA** (ANSI)<br/>               |



 

 





