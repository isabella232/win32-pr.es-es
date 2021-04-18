---
title: Códigos de error de animación de Windows (Winerror. h)
description: Si se produce un error, la animación de Windows devuelve un código como un valor HRESULT. En esta sección se proporciona una lista de códigos de error específicos de la animación de Windows. Para obtener una lista de códigos de error COM generales, vea códigos de error COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695908"
---
# <a name="windows-animation-error-codes"></a>Códigos de error de animación de Windows

Si se produce un error, la animación de Windows devuelve un código como un valor **HRESULT** . En esta sección se proporciona una lista de códigos de error específicos de la animación de Windows. Para obtener una lista de códigos de error COM generales, vea [códigos de error com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ \_ no se pudo crear la UI E**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



No se pudo crear el objeto.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**se \_ ha \_ \_ llamado a shutdown E UI**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Se ha llamado al método [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) en el administrador de animaciones, lo que hace que el administrador de animaciones se cierre y todas las variables de animación y guiones gráficos que creó se liberen.

> [!Note]  
> No se puede llamar a ningún método en ningún objeto de animación después del [**cierre**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**\_reentrada \_ ilegal E interfaz de usuario \_**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



No se puede llamar a este método durante este tipo de devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**objeto de interfaz de usuario \_ E \_ \_ sellado**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Este objeto se ha sellado, por lo que ya no se permite este cambio.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_valor E de UI \_ \_ no \_ establecido**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



No se ha establecido nunca el valor solicitado y, por lo tanto, no se puede recuperar.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_valor E de UI \_ \_ no \_ determinado**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



No se puede determinar el valor solicitado.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**salida de UI \_ E \_ no válida \_**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Una devolución de llamada devolvió un parámetro de salida no válido.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**se esperaba una interfaz de usuario \_ E \_ booleana \_**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Una devolución de llamada devolvió un código de éxito distinto de S \_ OK o s \_ false.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**propietario de la interfaz de usuario \_ E \_ diferente \_**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Un parámetro que debe ser propiedad de este objeto es propiedad de un objeto diferente.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ coincidencia AMBIGUA de UI E \_**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Hay más de un elemento que coincide con los criterios de búsqueda.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**desbordamiento de la interfaz de usuario \_ E \_ FP \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Se ha producido un desbordamiento de punto flotante.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**interfaz de usuario \_ E \_ \_ subproceso incorrecto**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Solo se puede llamar a este método desde el subproceso que creó el objeto.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**IU \_ E \_ guion gráfico \_ activo**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



El guión gráfico está actualmente en la programación.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**\_guion gráfico de UI E \_ \_ no \_ reproduciendo**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



El guión gráfico no se está reproduciendo.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**\_E \_ iniciar \_ fotograma \_ clave \_ de la interfaz de usuario después del final**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



El fotograma clave inicial podría producirse después del fotograma clave final.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**fotograma clave de IU \_ E \_ End \_ \_ no \_ determinado**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Es posible que no sea posible determinar el tiempo del fotograma clave final cuando se alcanza el fotograma clave inicial.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**superposición de \_ \_ bucles E interfaz de usuario \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Dos partes repetidas de un guión gráfico pueden superponerse.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**transición E interfaz de usuario \_ \_ \_ ya \_ usada**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



La transición ya se ha agregado a un guion gráfico diferente o se ha agregado a un guion gráfico que ha terminado de reproducirse y se ha liberado.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**\_ \_ transición de UI E \_ no \_ en \_ guion gráfico**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



La transición no se ha agregado a ningún guion gráfico.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transición E interfaz de usuario con \_ \_ \_ Eclipse**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



La transición podría Eclipse al principio de otra transición en el guión gráfico.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**E/s de la interfaz de usuario antes de la \_ \_ \_ \_ última \_ actualización**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



La hora especificada es anterior a la hora pasada a la última actualización.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**el \_ cliente de temporizador E interfaz de usuario \_ ya está \_ \_ \_ conectado**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Este cliente ya está conectado a un temporizador.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista y la actualización de plataforma solo para aplicaciones de escritorio de Windows Vista \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Encabezado<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de animación de Windows](windows-animation-reference.md)
</dt> </dl>

 

