---
description: Los GUID de configuración de energía identifican los eventos de cambio de energía.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID de configuración de energía (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681020"
---
# <a name="power-setting-guids"></a>GUID de configuración de energía

La configuración de energía **GUID** s identifica los eventos de cambio de energía. En este tema se enumeran los **GUID** de configuración de energía para las notificaciones que son más útiles para las aplicaciones. Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento. La notificación se envía cada vez que cambia un valor de configuración.

Los **GUID** de configuración de energía se definen en Winnt. h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**origen de energía de GUID \_ ACDC \_ \_**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



La fuente de alimentación del sistema ha cambiado. El miembro de **datos** es un **valor DWORD** con valores de la enumeración de la [**\_ \_ condición de energía del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) que indica la fuente de alimentación actual.

<dl> <dt>

**PoAc** (0): el equipo está equipado con una fuente de alimentación de corriente alterna (o similar, como un portátil equipado con un adaptador Automotive de 12V).
</dt> <dt>

**PoDc** (1): el equipo está equipado con una fuente de alimentación de batería incorporada.
</dt> <dt>

**PoHot** (2): el equipo está conectado a una fuente de alimentación a corto plazo, como un dispositivo SAI (UPS).
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_porcentaje de \_ batería \_ restante de GUID**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



La capacidad restante de la batería ha cambiado. La granularidad varía de un sistema a sistema, pero la granularidad más fina es del 1 por ciento. El miembro de **datos** es un **valor DWORD** que indica la capacidad de la batería actual que queda como porcentaje entre 0 y 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**Estado de visualización de la \_ consola GUID \_ \_**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



Ha cambiado el estado de visualización del monitor actual.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.

<dl> <dt>

0X0: la pantalla está desactivada.
</dt> <dt>

0x1: la pantalla está activada.
</dt> <dt>

0X2: la pantalla está atenuada.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_presencia de \_ usuario \_ global de GUID**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



El estado de usuario asociado con cualquier sesión ha cambiado. Representa el estado combinado de la presencia del usuario en todas las sesiones locales y remotas del sistema.

Esta notificación solo se envía a los servicios y a otros programas que se ejecutan en la sesión 0. En su lugar, las aplicaciones de modo de usuario deben registrarse en **\_ presencia de \_ usuario \_ de sesión GUID** .

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.

<dl> <dt>

**PowerUserPresent** (0): el usuario está presente en cualquier sesión local o remota del sistema.
</dt> <dt>

**PowerUserInactive** (2): el usuario no está presente en ninguna sesión local o remota del sistema.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_ \_ tarea en segundo plano de GUID inactivo \_**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



El sistema está ocupado. Esto indica que el sistema no pasará a un estado de inactividad en un futuro próximo y que la hora actual es un buen momento para que los componentes realicen tareas en segundo plano o inactivas que, de lo contrario, impedirían que el equipo entrara en estado de inactividad.

No hay ninguna notificación cuando el sistema puede pasar a un estado de inactividad. La notificación de tarea en segundo plano Inactiva no indica si un usuario está presente en el equipo. El miembro de **datos** no tiene información y se puede omitir.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ encendido del monitor \_ de GUID**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



El monitor de sistema principal se ha encendido o apagado. Esta notificación es útil para los componentes que representan activamente el contenido en el dispositivo de pantalla, como la visualización multimedia. Estas aplicaciones deben registrarse para esta notificación y dejar de representar el contenido de los gráficos cuando el monitor está apagado para reducir el consumo de energía del sistema. El miembro de **datos** es un **valor DWORD** que indica el estado actual del monitor.

<dl> <dt>

0X0: el monitor está desactivado.
</dt> <dt>

0x1: el monitor está activado.
</dt> </dl>

**Windows 8 y Windows Server 2012:** Las nuevas aplicaciones deben usar el estado de visualización de la **\_ consola \_ \_ GUID** en lugar de esta notificación.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_Estado de \_ ahorro de energía de GUID \_**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



El ahorro de batería se ha desactivado o está activado en respuesta a las condiciones de energía variables. Esta notificación es útil para los componentes que participan en el ahorro energético. Estas aplicaciones deben registrarse para esta notificación y ahorrar energía cuando el ahorro de batería está encendido.

El miembro de **datos** es un **valor DWORD** que indica el estado del ahorro de batería.

<dl> <dt>

0X0: el ahorro de batería está desactivado.
</dt> <dt>

0x1: el ahorro de batería está activado. Ahorre Energía siempre que sea posible.
</dt> </dl>

Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalidad POWERSCHEME de GUID \_**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



La personalidad de la combinación de energía activa ha cambiado. Todos los esquemas de energía se asignan a uno de estos personalidades. El miembro de **datos** es un **GUID** que indica la personalidad del nuevo plan de energía activo.

<dl> <dt>



**GUID \_ de \_ \_ Ahorro de energía mínimo** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Alto rendimiento: el esquema está diseñado para ofrecer el máximo rendimiento a costa del ahorro en el consumo de energía.


</dt> <dt>



**GUID \_ de \_ \_ Ahorro de energía máximo** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Economizador de energía: el esquema está diseñado para ofrecer el máximo ahorro de consumo de energía a costa del rendimiento y la capacidad de respuesta del sistema.


</dt> <dt>



**GUID \_ de \_ \_ Ahorro de energía típico** (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automático: el esquema está diseñado para equilibrar automáticamente el rendimiento y el ahorro de consumo de energía.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_Estado de \_ visualización de sesión GUID \_**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



La presentación asociada a la sesión de la aplicación se ha encendido o apagado.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

Esta notificación se envía solo a las aplicaciones de modo de usuario. Los servicios y otros programas que se ejecutan en la sesión 0 no reciben esta notificación. El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.

<dl> <dt>

0X0: la pantalla está desactivada.
</dt> <dt>

0x1: la pantalla está activada.
</dt> <dt>

0X2: la pantalla está atenuada.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_presencia de \_ usuario de sesión GUID \_**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



El estado de usuario asociado con la sesión de la aplicación ha cambiado.

**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

Esta notificación se envía solo a las aplicaciones de modo de usuario que se ejecutan en una sesión interactiva. Los servicios y otros programas que se ejecutan en la sesión 0 deben registrarse para la **\_ \_ \_ presencia de usuario global GUID**. El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.

<dl> <dt>

**PowerUserPresent** (0): el usuario proporciona la entrada a la sesión.
</dt> <dt>

**PowerUserInactive** (2): el tiempo de espera de la actividad de usuario ha transcurrido sin ninguna interacción del usuario.
</dt> </dl>

> [!Note]  
> Todas las aplicaciones que se ejecutan en una sesión interactiva en modo usuario deben usar esta opción. Cuando las aplicaciones en modo kernel se registran para el estado del monitor, deben usar el estado de presentación de la **\_ consola \_ \_ GUID** en su lugar.

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_AWAYMODE del sistema GUID \_**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



El sistema entra o sale del modo de ubicación. El miembro de **datos** es un **valor DWORD** que indica el estado del modo de ubicación actual.

<dl> <dt>

0X0: el equipo está saliendo del modo de ubicación.
</dt> <dt>

0x1: el equipo está entrando en modo de ubicación.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

