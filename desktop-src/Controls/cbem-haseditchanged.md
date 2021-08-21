---
title: CBEM_HASEDITCHANGED mensaje (Commctrl.h)
description: Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5949827dbabf962ec9a9e9bd9d3b6d27d09a3b7e62f7fc71f2c4343e8ce370
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528045"
---
# <a name="cbem_haseditchanged-message"></a>Mensaje \_ HASEDITCHANGED de CBEM

Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se ha cambiado el texto del cuadro de edición del control o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Un control ComboBoxEx usa un control de cuadro de edición cuando se establece en el estilo [**\_ DROPDOWN de CBS.**](combo-box-styles.md) Puede recuperar el identificador de ventana del control de cuadro de edición mediante el envío de un [**mensaje \_ GETEDITCONTROL de CBEM.**](cbem-geteditcontrol.md)

Cuando el usuario empiece a editar, recibirá una notificación [ \_ BEGINEDIT de CBEN.](cben-beginedit.md) Cuando se complete la edición o cambie el foco, recibirá una notificación [ \_ ENDEDIT de CBEN.](cben-endedit.md) El **mensaje \_ HASEDITCHANGED de CBEM** solo es útil para determinar si el texto se ha cambiado si se envía antes de la notificación \_ ENDEDIT de CBEN. Si el mensaje se envía después, devolverá **FALSE.** Por ejemplo, suponga que el usuario comienza a editar el texto en el cuadro de edición, pero cambia el foco, generando una notificación \_ ENDEDIT de CBEN. Si, a continuación, envía un **mensaje \_ HASEDITCHANGED de CBEM,** devolverá **FALSE,** aunque se haya cambiado el texto.

El [**estilo SIMPLE de \_ CBS**](combo-box-styles.md) no funciona correctamente con **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





