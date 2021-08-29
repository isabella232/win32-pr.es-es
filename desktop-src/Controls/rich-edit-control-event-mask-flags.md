---
title: Rich Edit Control Event Mask Flags (RichEdit.h)
description: La máscara de eventos especifica qué códigos de notificación envía un control de edición enriquecido a su ventana primaria. La máscara de evento puede ser ninguna o una combinación de estos valores.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92fe4be97a1288012b6a692f8837388e5eb4c99b465f1f34bb37d47ea0d44f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434805"
---
# <a name="rich-edit-control-event-mask-flags"></a>Marcas de máscara de eventos del control Rich Edit

La máscara de eventos especifica qué códigos de notificación envía un control de edición enriquecido a su ventana primaria. La máscara de evento puede ser ninguna o una combinación de estos valores.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**CAMBIO DE \_ ENM**</dt> </dl>                                  | Envía [notificaciones EN \_ CHANGE.](en-change--rich-edit-control-.md)<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ENM \_ CLIPFORMAT**</dt> </dl>                      | Envía [notificaciones EN \_ CLIPFORMAT.](/windows/desktop/Controls/en-clipformat)<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**ENM \_ CORRECTTEXT**</dt> </dl>                   | Envía [notificaciones EN \_ CORRECTTEXT.](en-correcttext.md)<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**ENM \_ DRAGDROPDONE**</dt> </dl>                | Envía [notificaciones EN \_ DRAGDROPDONE.](en-dragdropdone.md)<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**DROPFILES DE ENM \_**</dt> </dl>                         | Envía [notificaciones \_ EN DROPFILES.](en-dropfiles.md)<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**ENM \_ IMECHANGE**</dt> </dl>                         | Solo Microsoft Rich Edit 1.0: envía notificaciones [ \_ EN IMECHANGE](en-imechange.md) cuando el estado de conversión de IME ha cambiado. Solo para las versiones en idioma asiático del sistema operativo.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**ENM \_ KEYEVENTS**</dt> </dl>                         | Envía [notificaciones EN \_ MSGFILTER](en-msgfilter.md) para eventos de teclado.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**VÍNCULO DE \_ ENM**</dt> </dl>                                        | **Rich Edit 2.0 y versiones posteriores:** Envía [notificaciones EN \_ LINK](en-link.md) cuando el puntero del mouse está sobre el texto que tiene CFE LINK y se realiza una de varias \_ acciones del mouse.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**ENM \_ LOWFIRTF**</dt> </dl>                            | Envía [notificaciones \_ EN LOWFIRTF.](en-lowfirtf.md)<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**ENM \_ MOUSEEVENTS**</dt> </dl>                   | Envía [notificaciones EN \_ MSGFILTER](en-msgfilter.md) para eventos del mouse.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**ENM \_ OBJECTPOSITIONS**</dt> </dl>       | Envía [notificaciones EN \_ OBJECTPOSITIONS.](en-objectpositions.md)<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**PÁRRAFO \_ DE ENMEXPANDED**</dt> </dl> | Envía [notificaciones EN \_ PARAGRAPHEXPANDED.](/windows/desktop/Controls/en-paragraphexpanded)<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ENM \_ PROTECTED**</dt> </dl>                         | Envía [notificaciones EN \_ PROTECTED.](en-protected.md)<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**SOLICITUD DE \_ ENMRESIZE**</dt> </dl>             | Envía [notificaciones EN \_ REQUESTRESIZE.](en-requestresize.md)<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**DESPLAZAMIENTO \_ DE ENM**</dt> </dl>                                  | Envía [notificaciones EN \_ HSCROLL](en-hscroll.md) [y EN \_ VSCROLL.](en-vscroll.md)<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**EVENTOS DE DESPLAZAMIENTO DE ENM \_**</dt> </dl>                | Envía [notificaciones EN \_ MSGFILTER](en-msgfilter.md) para eventos de rueda del mouse.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**ENM \_ SELCHANGE**</dt> </dl>                         | Envía [notificaciones \_ EN SELCHANGE.](en-selchange.md)<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**ACTUALIZACIÓN DE \_ ENM**</dt> </dl>                                  | Envía [notificaciones EN \_ UPDATE.](en-update.md) <br/> **Rich Edit 2.0 y versiones posteriores:** esta marca se omite y siempre se envían las notificaciones [EN \_ UPDATE.](en-update.md) Sin embargo, si Rich Edit 3.0 emula Microsoft Rich Edit 1.0, debe usar esta marca para enviar notificaciones EN \_ UPDATE.<br/> |



## <a name="remarks"></a>Observaciones

La máscara de evento predeterminada es ENM NONE, en cuyo caso no se envía \_ ninguna notificación a la ventana primaria. Puede recuperar y establecer la máscara de eventos para un control de edición enriquecido mediante los mensajes [**EM \_ GETEVENTMASK**](em-geteventmask.md) y [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>RichEdit.h</dt> </dl> |



 

