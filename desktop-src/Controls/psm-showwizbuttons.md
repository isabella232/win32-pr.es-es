---
title: PSM_SHOWWIZBUTTONS mensaje (Prsht.h)
description: Muestra u oculta los botones de un asistente. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167473"
---
# <a name="psm_showwizbuttons-message"></a>Mensaje \_ SHOWWIZBUTTONS de PSM

Muestra u oculta los botones de un asistente. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet ShowWizButtons.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o varios de los valores siguientes que especifican qué botones de hoja de propiedades se van a mostrar. Si se incluye un valor de botón en este parámetro y *lParam*, se muestra.



| Value                                                                                                                                                                                 | Significado                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIWI \_ BACK**</dt> </dl>                               | Botón  Atrás.<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIWI \_ CANCEL**</dt> </dl>                         | Botón **Cancelar.**<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIWIWI \_ DISABLEDFINISH**</dt> </dl> | Botón **Finalizar.**<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIWI \_ FINISH**</dt> </dl>                         | Botón **Finalizar.**<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIWI \_ NEXT**</dt> </dl>                               | Botón  Siguiente.<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIWIWI \_ SHOW**</dt> </dl>                               | Establezca solo esta marca (definida como cero) para ocultar todos los botones especificados *en lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**RESTAURACIÓN DE \_ PSWIWIWI**</dt> </dl>                      | Sin implementar.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o varios de los mismos valores usados en *wParam*, especificando qué botones se ven afectados por esta llamada. Si aparece un valor de botón en este parámetro pero no en *wParam*, el botón está oculto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los asistentes muestran tres o cuatro botones debajo de cada página. Este mensaje se usa para especificar qué botones están visibles. Normalmente, los asistentes **muestran los**  botones **Atrás,** Cancelar y Siguiente **o** Finalizar. El **botón** Cancelar siempre está visible.

Normalmente, establezca **PSWIWI \_ FINISH o** **PSWIPLACE \_ DISABLEDFINISH** para reemplazar el botón **Siguiente** por un **botón** Finalizar. Para mostrar  **los botones** Siguiente y Finalizar simultáneamente, establezca la marca **PSH \_ WIZARDHASFINISH** en el **miembro dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) al crear el asistente. A continuación, cada página mostrará los cuatro botones: **Atrás,** **Siguiente,** **Cancelar** y **Finalizar.**

Si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) para enviar este mensaje, se publicará. En cualquier otro momento, puede usar [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar **PSM \_ SHOWWIZBUTTONS**.

Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje **\_ SHOWWIZBUTTONS de PSM,** no haga nada que afecte al foco de ventana hasta que el controlador vuelva. Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para enviar **PSM \_ SHOWWIZBUTTONS,** el cuadro de mensaje recibirá el foco. Puesto que los mensajes publicados no se entregan hasta que llegan al principio de la cola de mensajes, el mensaje **\_ SHOWWIZBUTTONS** de PSM no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje. Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

