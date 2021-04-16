---
title: Mensaje de PSM_SHOWWIZBUTTONS (Prsht. h)
description: Muestra u oculta los botones en un asistente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656490"
---
# <a name="psm_showwizbuttons-message"></a>Mensaje de PSM \_ SHOWWIZBUTTONS

Muestra u oculta los botones en un asistente. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o varios de los siguientes valores que especifican qué botones de la hoja de propiedades se van a mostrar. Si un valor de botón está incluido en este parámetro y *lParam*, se muestra.



| Value                                                                                                                                                                                 | Significado                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ atrás**</dt> </dl>                               | Botón **atrás** .<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**\_Cancelar PSWIZB**</dt> </dl>                         | Botón **Cancelar** .<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | El botón **Finalizar** .<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_Finalizar PSWIZB**</dt> </dl>                         | El botón **Finalizar** .<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ siguiente**</dt> </dl>                               | Botón **siguiente** .<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ Mostrar**</dt> </dl>                               | Establezca solo esta marca (definida como cero) para ocultar todos los botones especificados en *lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**restauración de PSWIZB \_**</dt> </dl>                      | Sin implementar.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o varios de los mismos valores utilizados en *wParam*, que especifican qué botones se ven afectados por esta llamada. Si aparece un valor de botón en este parámetro pero no en *wParam*, el botón está oculto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los asistentes muestran tres o cuatro botones debajo de cada página. Este mensaje se usa para especificar qué botones son visibles. Los asistentes muestran normalmente **atrás**, **Cancelar** y un botón **siguiente** o **Finalizar** . El botón **Cancelar** siempre está visible.

Normalmente, establezca **PSWIZB \_ Finish** o **PSWIZB \_ DISABLEDFINISH** para reemplazar el botón **siguiente** por un botón **Finalizar** . Para mostrar los botones **siguiente** y **Finalizar** simultáneamente, establezca la marca **PSH \_ WIZARDHASFINISH** en el miembro **dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) al crear el asistente. Cada página mostrará los cuatro botones: **atrás**, **siguiente**, **Cancelar** y **Finalizar**.

Si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) para enviar este mensaje, se publicará. En cualquier otro momento, puede usar [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar **PSM \_ SHOWWIZBUTTONS**.

Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de **PSM \_ SHOWWIZBUTTONS** , no haga nada que afecte al foco de la ventana hasta después de que se devuelva el controlador. Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para **enviar \_ PSM SHOWWIZBUTTONS**, el cuadro de mensaje recibirá el foco. Dado que los mensajes expuestos no se entregan hasta que alcanzan el encabezado de la cola de mensajes, el mensaje de **PSM \_ SHOWWIZBUTTONS** no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje. Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

