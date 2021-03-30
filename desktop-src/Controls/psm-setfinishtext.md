---
title: Mensaje de PSM_SETFINISHTEXT (Prsht. h)
description: Establece el texto del botón Finalizar en un asistente, muestra y habilita el botón, y oculta los botones siguiente y atrás. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801225"
---
# <a name="psm_setfinishtext-message"></a>Mensaje de PSM \_ SETFINISHTEXT

Establece el texto del botón **Finalizar** en un asistente, muestra y habilita el botón, y oculta los botones **siguiente** y **atrás** . Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al nuevo texto para el botón **Finalizar** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el botón **Finalizar** no tiene una tecla de aceleración. Puede crear una tecla de aceleración con este mensaje incluyendo una y comercial (&) en la cadena de texto que asigna a *lParam*. Por ejemplo, "&Finish" define F como la tecla de aceleración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) y **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





