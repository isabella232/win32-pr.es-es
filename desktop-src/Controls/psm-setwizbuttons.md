---
title: PSM_SETWIZBUTTONS mensaje (Prsht.h)
description: Habilita o deshabilita los botones Atrás, Siguiente y Finalizar en un asistente. También puede usar la macro PropSheet \_ SetWizButtons para publicar el mensaje.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167477"
---
# <a name="psm_setwizbuttons-message"></a>Mensaje \_ SETWIZBUTTONS de PSM

Habilita o deshabilita los botones **Atrás,** **Siguiente** **y Finalizar** en un asistente. También puede usar la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para publicar el mensaje.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establezca este parámetro en PSWIOGRAFÍAF ELEVATIONREQUIRED para mostrar el icono con privilegios elevados en los \_ botones especificados en *lParam*. El icono con privilegios elevados (o icono de escudo de UAC) indica que el símbolo del sistema de elevación se usará para solicitar al usuario la aprobación o las credenciales. Para obtener más información, [vea Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> La visualización del icono de escudo de UAC solo se admite en AeroWizards (PSH \_ AEROWIZARD).

 

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica qué botones de hoja de propiedades están habilitados. Puede combinar una o varias de las marcas siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIWI \_ BACK**</dt> </dl>                               | Habilita el **botón** Atrás. Si no se establece esta marca, el **botón** Atrás se muestra como deshabilitado.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIWIWI \_ DISABLEDFINISH**</dt> </dl> | Muestra un botón **Finalizar** deshabilitado.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIWI \_ FINISH**</dt> </dl>                         | Muestra un botón **Finalizar** habilitado.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIWI \_ NEXT**</dt> </dl>                               | Habilita el botón **Siguiente**. Si no se establece esta marca, **el** botón Siguiente se muestra como deshabilitado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el controlador de notificaciones usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) para enviar un mensaje **\_ SETWIZBUTTONS de PSM,** no haga nada que afecte al foco de ventana hasta que el controlador vuelva. Por ejemplo, si llama a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) inmediatamente después de usar **PostMessage** para enviar **PSM \_ SETWIZBUTTONS,** el cuadro de mensaje recibirá el foco. Puesto que los mensajes publicados no se entregan hasta que llegan al principio de la cola de mensajes, el mensaje **\_ SETWIZBUTTONS** de PSM no se entregará hasta que el asistente haya perdido el foco en el cuadro de mensaje. Como resultado, la hoja de propiedades no podrá establecer correctamente el foco de los botones.

Si envía el mensaje SETWIZBUTTONS de PSM durante el control de la notificación \_ [ \_ SETACTIVE de PSN,](psn-setactive.md) use la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) en lugar de la [**función SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) De lo contrario, el sistema no actualizará los botones correctamente. Si usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para enviar este mensaje, se publicará. En cualquier otro momento, puede usar **SendMessage** para enviar **PSM \_ SETWIZBUTTONS**.

Los asistentes muestran tres o cuatro botones debajo de cada página. Este mensaje se usa para especificar qué botones están habilitados. Normalmente, los asistentes **muestran los**  botones **Atrás,** Cancelar y Siguiente **o** Finalizar. Normalmente solo se habilita el botón **Siguiente**  para la página de bienvenida, **Siguiente** y Atrás para las páginas interiores y Atrás **y** **Finalizar** para la página de finalización. El **botón** Cancelar siempre está habilitado. Normalmente, al establecer PSWIWI \_ FINISH o PSWIWI DISABLEDFINISH se reemplaza el botón Siguiente \_ por un botón **Finalizar.**  Para mostrar  **los** botones Siguiente y Finalizar simultáneamente, establezca la marca PSH \_ WIZARDHASFINISH en el **miembro dwFlags** de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) del asistente al crear el asistente. A continuación, cada página mostrará los cuatro botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

