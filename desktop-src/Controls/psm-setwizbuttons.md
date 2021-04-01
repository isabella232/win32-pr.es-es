---
title: Mensaje de PSM_SETWIZBUTTONS (Prsht. h)
description: Habilita o deshabilita los botones atrás, siguiente y finalizar en un asistente. También puede usar la macro PropSheet \_ SetWizButtons para publicar el mensaje.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150457"
---
# <a name="psm_setwizbuttons-message"></a>Mensaje de PSM \_ SETWIZBUTTONS

Habilita o deshabilita los botones **atrás**, **siguiente** y **Finalizar** en un asistente. También puede usar la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para publicar el mensaje.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establezca este parámetro en PSWIZBF \_ ELEVATIONREQUIRED para mostrar el icono con privilegios elevados en los botones especificados en *lParam*. El icono con privilegios elevados (o el icono de escudo de UAC) indica que se utilizará la petición de elevación para solicitar la aprobación del usuario o las credenciales. Para obtener más información, vea [diseñar aplicaciones de UAC para Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> La visualización del icono de escudo de UAC solo se admite en AeroWizards (PSH \_ AEROWIZARD).

 

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica qué botones de la hoja de propiedades están habilitados. Puede combinar una o varias de las marcas siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ atrás**</dt> </dl>                               | Habilita el botón **atrás** . Si no se establece esta marca, el botón **atrás** se muestra como deshabilitado.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Muestra un botón **Finalizar** deshabilitado.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_Finalizar PSWIZB**</dt> </dl>                         | Muestra un botón **Finalizar** habilitado.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ siguiente**</dt> </dl>                               | Habilita el botón **Siguiente**. Si no se establece esta marca, el botón **siguiente** se muestra como deshabilitado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de **PSM \_ SETWIZBUTTONS** , no haga nada que afecte al foco de la ventana hasta después de que se devuelva el controlador. Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para **enviar \_ PSM SETWIZBUTTONS**, el cuadro de mensaje recibirá el foco. Dado que los mensajes expuestos no se entregan hasta que alcanzan el encabezado de la cola de mensajes, el mensaje de **PSM \_ SETWIZBUTTONS** no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje. Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.

Si envía el \_ mensaje de PSM SETWIZBUTTONS durante el control de la notificación de [PSN \_ SETACTIVE](psn-setactive.md) , use la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) en lugar de la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . De lo contrario, el sistema no actualizará los botones correctamente. Si usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para enviar este mensaje, se publicará. En cualquier otro momento, puede usar **SendMessage** para enviar **PSM \_ SETWIZBUTTONS**.

Los asistentes muestran tres o cuatro botones debajo de cada página. Este mensaje se usa para especificar qué botones están habilitados. Los asistentes muestran normalmente **atrás**, **Cancelar** y un botón **siguiente** o **Finalizar** . Normalmente, solo se habilita el botón **siguiente** de la Página principal, **siguiente** y **atrás** para las páginas interiores y **atrás** y **Finalizar** para la página de finalización. El botón **Cancelar** siempre está habilitado. Normalmente, al establecer PSWIZB \_ Finish o PSWIZB DISABLEDFINISH, se \_ reemplaza el botón **siguiente** con un botón **Finalizar** . Para mostrar los botones **siguiente** y **Finalizar** simultáneamente, establezca la \_ marca PSH WIZARDHASFINISH en el miembro **dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) del asistente al crear el asistente. Cada página mostrará los cuatro botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

