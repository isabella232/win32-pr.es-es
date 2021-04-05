---
title: Mensaje de CBEM_HASEDITCHANGED (commctrl. h)
description: Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED controles de mensajes de Windows
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
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997116"
---
# <a name="cbem_haseditchanged-message"></a>CBEM \_ HASEDITCHANGED

Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha cambiado el texto del cuadro de edición del control o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Un control ComboBoxEx usa un control de cuadro de edición cuando se establece en el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) . Puede recuperar el identificador de ventana del control del cuadro de edición mediante el envío de un mensaje de [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .

Cuando el usuario empiece a editar, recibirá una notificación de [CBEN \_ BEGINEDIT](cben-beginedit.md) . Una vez completada la edición o cambia el foco, recibirá una notificación de [CBEN \_ ENDEDIT](cben-endedit.md) . El mensaje **CBEM \_ HASEDITCHANGED** solo es útil para determinar si se ha cambiado el texto en caso de que se envíe antes de la \_ notificación CBEN ENDEDIT. Si el mensaje se envía después, devolverá **false**. Por ejemplo, supongamos que el usuario comienza a editar el texto en el cuadro de edición pero cambia el foco, generando una notificación de CBEN \_ ENDEDIT. Si, a continuación, envía un mensaje **\_ HASEDITCHANGED de CBEM** , devolverá **false**, aunque el texto se haya cambiado.

El [**estilo \_ simple CBS**](combo-box-styles.md) no funciona correctamente con **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





