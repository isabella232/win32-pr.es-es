---
description: Los GUID de configuración de energía identifican los eventos de cambio de energía.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID de configuración de energía (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b05909509e0c3ed581582ebe90b10e5df4e91a31b7ab050b3fd1ef6679b1a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887035"
---
# <a name="power-setting-guids"></a>GUID de configuración de energía

Los **GUID** de configuración de energía identifican eventos de cambio de energía. En este tema se enumeran **los GUID de configuración** de energía para las notificaciones que son más útiles para las aplicaciones. Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento. La notificación se envía cada vez que cambia una configuración.

Los **GUID de configuración** de energía se definen en WinNT.h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**FUENTE \_ DE ALIMENTACIÓN DEL ACDC \_ \_ GUID**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



La fuente de alimentación del sistema ha cambiado. El **miembro** Data es un **DWORD con** valores de la [**enumeración SYSTEM POWER \_ \_ CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) que indica la fuente de alimentación actual.

<dl> <dt>

**PoAc** (0): el equipo está encendido por una fuente de alimentación de CA (o similar, como un portátil con tecnología de un adaptador de automoción de 12 V).
</dt> <dt>

**PoDc** (1): el equipo está encendido por una fuente de alimentación de batería incorporada.
</dt> <dt>

**PoHot** (2): el equipo funciona con una fuente de alimentación a corto plazo, como un dispositivo UPS.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**PORCENTAJE RESTANTE \_ DE \_ BATERÍA GUID \_**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-LOBB468A9E1
</dt> <dt>



La capacidad restante de la batería ha cambiado. La granularidad varía de sistema a sistema, pero la granularidad más fina es del 1 %. El **miembro** Data es un **DWORD** que indica la capacidad de batería actual restante como porcentaje de 0 a 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**ESTADO DE \_ PRESENTACIÓN DE LA CONSOLA \_ \_ GUID**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



El estado de presentación del monitor actual ha cambiado.

**Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

El **miembro** Data es **un DWORD** con uno de los valores siguientes.

<dl> <dt>

0x0: la pantalla está desactivada.
</dt> <dt>

0x1: la pantalla está en.
</dt> <dt>

0x2: la pantalla está atenuada.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**PRESENCIA \_ GLOBAL DE USUARIOS \_ \_ GUID**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



El estado de usuario asociado a cualquier sesión ha cambiado. Esto representa el estado combinado de presencia del usuario en todas las sesiones locales y remotas del sistema.

Esta notificación solo se envía a los servicios y otros programas que se ejecutan en la sesión 0. En su lugar, las aplicaciones en modo de usuario deben registrarse **para LA PRESENCIA DEL USUARIO DE LA SESIÓN \_ \_ \_ GUID.**

**Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

El **miembro** Data es **un DWORD** con uno de los valores siguientes.

<dl> <dt>

**PowerUserPresent** (0): el usuario está presente en cualquier sesión local o remota del sistema.
</dt> <dt>

**PowerUserInactive** (2): el usuario no está presente en ninguna sesión local o remota del sistema.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**TAREA EN \_ \_ SEGUNDO PLANO DE \_ INACTIVIDAD DE GUID**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



El sistema está ocupado. Esto indica que el sistema no pasará a un estado de inactividad en un futuro próximo y que la hora actual es un buen momento para que los componentes realicen tareas en segundo plano o inactivas que, de lo contrario, impedirían que el equipo entrara en un estado de inactividad.

No hay ninguna notificación cuando el sistema puede pasar a un estado de inactividad. La notificación de tarea en segundo plano inactiva no indica si un usuario está presente en el equipo. El **miembro** Data no tiene información y se puede omitir.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**ENCENDIDO \_ DEL MONITOR \_ \_ GUID**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



El monitor del sistema principal se ha encendido o apagado. Esta notificación es útil para los componentes que representan activamente el contenido en el dispositivo de visualización, como la visualización multimedia. Estas aplicaciones deben registrarse para esta notificación y dejar de representar contenido gráfico cuando el monitor está desactivado para reducir el consumo de energía del sistema. El **miembro** Data es **un DWORD** que indica el estado del monitor actual.

<dl> <dt>

0x0: el monitor está desactivado.
</dt> <dt>

0x1: el monitor está en.
</dt> </dl>

**Windows 8 y Windows Server 2012:** Las nuevas aplicaciones deben usar **EL ESTADO DE VISUALIZACIÓN DE LA CONSOLA \_ \_ \_ GUID** en lugar de esta notificación.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**ESTADO DE \_ AHORRO DE ENERGÍA DE \_ \_ GUID**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



El ahorro de batería se ha apagado o activado en respuesta a las condiciones de energía cambiantes. Esta notificación es útil para los componentes que participan en la conservación de energía. Estas aplicaciones deben registrarse para esta notificación y ahorrar energía cuando ahorro de batería está encendido.

El **miembro** Data es **un DWORD** que indica ahorro de batería estado.

<dl> <dt>

0x0: el ahorro de batería está apagado.
</dt> <dt>

0x1: el ahorro de batería está activado. Ahorre energía siempre que sea posible.
</dt> </dl>

Para obtener información general sobre ahorro de batería, [vea ahorro de batería (en las directrices de componentes de hardware).](/windows-hardware/design/component-guidelines/battery-saver)

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID \_ POWERSCHEME \_ PERSONALITY**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



La personalidad del esquema de energía activo ha cambiado. Todos los esquemas de energía se asignan a una de estas personalidades. El **miembro** Data es un **GUID** que indica la nueva personalidad del esquema de energía activo.

<dl> <dt>



**GUID \_ AHORRO \_ MÍNIMO \_ DE ENERGÍA** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Alto rendimiento: el esquema está diseñado para ofrecer el máximo rendimiento a costa del ahorro de consumo de energía.


</dt> <dt>



**GUID \_ MAX \_ POWER \_ SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)

Ahorro de energía: el esquema está diseñado para ofrecer el máximo ahorro de consumo de energía a costa del rendimiento y la capacidad de respuesta del sistema.


</dt> <dt>



**GUID \_ AHORRO \_ DE \_ ENERGÍA** TÍPICO (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automático: el esquema está diseñado para equilibrar automáticamente el rendimiento y el ahorro de consumo de energía.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**ESTADO DE \_ PRESENTACIÓN DE LA SESIÓN \_ \_ GUID**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



La pantalla asociada a la sesión de la aplicación se ha encendido o desactivado.

**Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

Esta notificación solo se envía a las aplicaciones en modo de usuario. Los servicios y otros programas que se ejecutan en la sesión 0 no reciben esta notificación. El **miembro** Data es **un DWORD** con uno de los valores siguientes.

<dl> <dt>

0x0: la pantalla está desactivada.
</dt> <dt>

0x1: la pantalla está en.
</dt> <dt>

0x2: la pantalla está atenuada.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**PRESENCIA DEL \_ USUARIO DE LA SESIÓN \_ \_ GUID**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



El estado de usuario asociado a la sesión de la aplicación ha cambiado.

**Windows 7, Windows Server 2008 R2, Windows Vista y Windows Server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.

Esta notificación solo se envía a las aplicaciones en modo de usuario que se ejecutan en una sesión interactiva. Los servicios y otros programas que se ejecutan en la sesión 0 deben registrarse para **GUID \_ GLOBAL USER \_ \_ PRESENCE**. El **miembro** Data es **un DWORD** con uno de los valores siguientes.

<dl> <dt>

**PowerUserPresent** (0): el usuario proporciona datos de entrada a la sesión.
</dt> <dt>

**PowerUser Periodo** (2): el tiempo de espera de actividad del usuario ha transcurrido sin interacción del usuario.
</dt> </dl>

> [!Note]  
> Todas las aplicaciones que se ejecutan en una sesión interactiva en modo de usuario deben usar esta configuración. Cuando las aplicaciones en modo kernel se registran para el estado de supervisión, deben usar **EL ESTADO DE VISUALIZACIÓN DE LA CONSOLA GUID \_ \_ \_ en** su lugar.

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID \_ SYSTEM \_ AWAYMODE**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



El sistema entra o sale del modo. El **miembro** Data es un **DWORD** que indica el estado del modo de distancia actual.

<dl> <dt>

0x0: el equipo está saliendo del modo.
</dt> <dt>

0x1: el equipo entra en modo de distancia.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WinNT.h</dt> </dl> |



 

