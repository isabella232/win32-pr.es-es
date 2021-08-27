---
title: PSM_SETFINISHTEXT mensaje (Prsht.h)
description: Establece el texto del botón Finalizar en un asistente, muestra y habilita el botón y oculta los botones Siguiente y Atrás. Puede enviar este mensaje explícitamente o mediante la \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT controles de Windows mensaje
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
ms.openlocfilehash: 5a08cafbeafeccb2235cb9b653f997aa8c60bd5fd21a3ccbc92e572fa5d3d0db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088565"
---
# <a name="psm_setfinishtext-message"></a>Mensaje \_ SETFINISHTEXT de PSM

Establece el texto del botón **Finalizar** en un asistente, muestra y habilita el botón y oculta los botones **Siguiente** **y** Atrás. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet SetFinishText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al nuevo texto del **botón** Finalizar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

De forma predeterminada, **el botón** Finalizar no tiene un acelerador de teclado. Puede crear un acelerador de teclado con este mensaje si incluye una yerba (&) en la cadena de texto que asigna a *lParam*. Por ejemplo, "&Finalizar" define F como tecla de aceleración.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) y **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





