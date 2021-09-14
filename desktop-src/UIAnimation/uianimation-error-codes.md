---
title: Windows Códigos de error de animación (Winerror.h)
description: Si se produce un error, Windows Animation devuelve un código como un valor HRESULT. En esta sección se proporciona una lista de códigos de error específicos de Windows Animation. Para obtener una lista de códigos de error COM generales, vea Códigos de error COM.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242066"
---
# <a name="windows-animation-error-codes"></a>Windows Códigos de error de animación

Si se produce un error, Windows Animation devuelve un código como **un valor HRESULT.** En esta sección se proporciona una lista de códigos de error específicos de Windows Animation. Para obtener una lista de códigos de error COM generales, vea [Códigos de error COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**ERROR EN \_ LA CREACIÓN DE LA INTERFAZ DE USUARIO \_ \_ E**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



No se pudo crear el objeto.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI \_ E \_ SHUTDOWN \_ CALLED**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



Se [**ha llamado**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) al método Shutdown en el administrador de animación, lo que hace que el administrador de animaciones se apague y se liberarán todas las variables de animación y guiones gráficos que creó.

> [!Note]  
> No se puede llamar a ningún método en ningún objeto de animación después de [**apagar**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**\_ \_ REENENLACE NO ES DE LA INTERFAZ DE USUARIO \_ E**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



No se puede llamar a este método durante este tipo de devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**OBJETO \_ E DE INTERFAZ DE USUARIO \_ \_ SELLADO**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Este objeto se ha sellado, por lo que este cambio ya no se permite.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**VALOR \_ E DE LA INTERFAZ DE USUARIO NO \_ \_ \_ ESTABLECIDO**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



El valor solicitado nunca se ha establecido y, por tanto, no se puede recuperar.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**VALOR \_ E DE LA INTERFAZ DE USUARIO NO \_ \_ \_ DETERMINADO**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



No se puede determinar el valor solicitado.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**SALIDA NO \_ VÁLIDA DE LA INTERFAZ DE USUARIO \_ \_ E**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Una devolución de llamada devolvió un parámetro de salida no válido.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI \_ E \_ BOOLEAN \_ EXPECTED**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Una devolución de llamada devolvió un código correcto distinto de S \_ OK o S \_ FALSE.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**PROPIETARIO \_ DIFERENTE DE LA INTERFAZ DE USUARIO \_ \_ E**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Un parámetro que debe ser propiedad de este objeto pertenece a un objeto diferente.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI \_ E \_ AMBIGUOUS \_ MATCH**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Más de un elemento coincidió con los criterios de búsqueda.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP \_ OVERFLOW**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Se produjo un desbordamiento de punto flotante.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**SUBPROCESO \_ INCORRECTO DE LA INTERFAZ DE USUARIO \_ \_ E**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Solo se puede llamar a este método desde el subproceso que creó el objeto .


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**GUIÓN \_ GRÁFICO DE INTERFAZ DE USUARIO E \_ \_ ACTIVO**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



El guión gráfico está actualmente en la programación.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**GUIÓN \_ GRÁFICO DE IU E \_ NO \_ \_ REPRODUCIENDO**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



El guión gráfico no se está reproduciendo.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**FOTOGRAMA CLAVE \_ DE INICIO \_ DE \_ IU E DESPUÉS DEL \_ \_ FINAL**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



El fotograma clave inicial puede producirse después del fotograma clave final.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**FOTOGRAMA CLAVE \_ FINAL DE IU E \_ \_ NO \_ \_ DETERMINADO**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Es posible que no sea posible determinar la hora del fotograma clave final cuando se alcanza el fotograma clave inicial.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**SUPERPOSICIÓN \_ DE BUCLES E \_ DE INTERFAZ \_ DE USUARIO**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Dos partes repetidas de un guión gráfico pueden superponerse.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**TRANSICIÓN \_ DE IU E \_ YA \_ \_ USADA**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



La transición ya se ha agregado a un guión gráfico diferente o se ha agregado a un guión gráfico que ha terminado de reproducirse y se ha publicado.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**TRANSICIÓN \_ DE IU E \_ NO EN EL \_ \_ \_ GUIÓN GRÁFICO**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



La transición no se ha agregado a ningún guión gráfico.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**IU \_ E \_ TRANSITION \_ ECLIPSED**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



La transición podría eclipse el principio de otra transición en el guión gráfico.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**HORA \_ E DE LA INTERFAZ DE USUARIO ANTERIOR A LA ÚLTIMA \_ \_ \_ \_ ACTUALIZACIÓN**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



La hora especificada es anterior a la hora pasada a la última actualización.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**CLIENTE \_ DE TEMPORIZADOR E DE INTERFAZ DE USUARIO YA \_ \_ \_ \_ CONECTADO**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Este cliente ya está conectado a un temporizador.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows vista y actualización de plataforma solo para Windows de escritorio de Vista \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Encabezado<br/>                   | <dl> <dt>Winerror.h</dt> </dl>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Referencia de animación](windows-animation-reference.md)
</dt> </dl>

 

