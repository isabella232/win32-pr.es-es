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
# <a name="power-setting-guids"></a><span data-ttu-id="b4a6e-103">GUID de configuración de energía</span><span class="sxs-lookup"><span data-stu-id="b4a6e-103">Power Setting GUIDs</span></span>

<span data-ttu-id="b4a6e-104">La configuración de energía **GUID** s identifica los eventos de cambio de energía.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="b4a6e-105">En este tema se enumeran los **GUID** de configuración de energía para las notificaciones que son más útiles para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="b4a6e-106">Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="b4a6e-107">La notificación se envía cada vez que cambia un valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="b4a6e-108">Los **GUID** de configuración de energía se definen en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**origen de energía de GUID \_ ACDC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="b4a6e-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-111">La fuente de alimentación del sistema ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-111">The system power source has changed.</span></span> <span data-ttu-id="b4a6e-112">El miembro de **datos** es un **valor DWORD** con valores de la enumeración de la [**\_ \_ condición de energía del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) que indica la fuente de alimentación actual.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-113">**PoAc** (0): el equipo está equipado con una fuente de alimentación de corriente alterna (o similar, como un portátil equipado con un adaptador Automotive de 12V).</span><span class="sxs-lookup"><span data-stu-id="b4a6e-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-114">**PoDc** (1): el equipo está equipado con una fuente de alimentación de batería incorporada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-115">**PoHot** (2): el equipo está conectado a una fuente de alimentación a corto plazo, como un dispositivo SAI (UPS).</span><span class="sxs-lookup"><span data-stu-id="b4a6e-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_porcentaje de \_ batería \_ restante de GUID**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="b4a6e-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-118">La capacidad restante de la batería ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="b4a6e-119">La granularidad varía de un sistema a sistema, pero la granularidad más fina es del 1 por ciento.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="b4a6e-120">El miembro de **datos** es un **valor DWORD** que indica la capacidad de la batería actual que queda como porcentaje entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4a6e-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**Estado de visualización de la \_ consola GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="b4a6e-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-123">Ha cambiado el estado de visualización del monitor actual.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="b4a6e-124">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b4a6e-125">El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-126">0X0: la pantalla está desactivada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-127">0x1: la pantalla está activada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-128">0X2: la pantalla está atenuada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_presencia de \_ usuario \_ global de GUID**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="b4a6e-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-131">El estado de usuario asociado con cualquier sesión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="b4a6e-132">Representa el estado combinado de la presencia del usuario en todas las sesiones locales y remotas del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="b4a6e-133">Esta notificación solo se envía a los servicios y a otros programas que se ejecutan en la sesión 0.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="b4a6e-134">En su lugar, las aplicaciones de modo de usuario deben registrarse en **\_ presencia de \_ usuario \_ de sesión GUID** .</span><span class="sxs-lookup"><span data-stu-id="b4a6e-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="b4a6e-135">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b4a6e-136">El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-137">**PowerUserPresent** (0): el usuario está presente en cualquier sesión local o remota del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-138">**PowerUserInactive** (2): el usuario no está presente en ninguna sesión local o remota del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_ \_ tarea en segundo plano de GUID inactivo \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="b4a6e-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-141">El sistema está ocupado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-141">The system is busy.</span></span> <span data-ttu-id="b4a6e-142">Esto indica que el sistema no pasará a un estado de inactividad en un futuro próximo y que la hora actual es un buen momento para que los componentes realicen tareas en segundo plano o inactivas que, de lo contrario, impedirían que el equipo entrara en estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="b4a6e-143">No hay ninguna notificación cuando el sistema puede pasar a un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="b4a6e-144">La notificación de tarea en segundo plano Inactiva no indica si un usuario está presente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="b4a6e-145">El miembro de **datos** no tiene información y se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4a6e-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ encendido del monitor \_ de GUID**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="b4a6e-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-148">El monitor de sistema principal se ha encendido o apagado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="b4a6e-149">Esta notificación es útil para los componentes que representan activamente el contenido en el dispositivo de pantalla, como la visualización multimedia.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="b4a6e-150">Estas aplicaciones deben registrarse para esta notificación y dejar de representar el contenido de los gráficos cuando el monitor está apagado para reducir el consumo de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="b4a6e-151">El miembro de **datos** es un **valor DWORD** que indica el estado actual del monitor.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-152">0X0: el monitor está desactivado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-153">0x1: el monitor está activado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="b4a6e-154">**Windows 8 y Windows Server 2012:** Las nuevas aplicaciones deben usar el estado de visualización de la **\_ consola \_ \_ GUID** en lugar de esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_Estado de \_ ahorro de energía de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="b4a6e-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-157">El ahorro de batería se ha desactivado o está activado en respuesta a las condiciones de energía variables.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="b4a6e-158">Esta notificación es útil para los componentes que participan en el ahorro energético.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="b4a6e-159">Estas aplicaciones deben registrarse para esta notificación y ahorrar energía cuando el ahorro de batería está encendido.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="b4a6e-160">El miembro de **datos** es un **valor DWORD** que indica el estado del ahorro de batería.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-161">0X0: el ahorro de batería está desactivado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-162">0x1: el ahorro de batería está activado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="b4a6e-163">Ahorre Energía siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="b4a6e-164">Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="b4a6e-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalidad POWERSCHEME de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="b4a6e-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-167">La personalidad de la combinación de energía activa ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="b4a6e-168">Todos los esquemas de energía se asignan a uno de estos personalidades.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="b4a6e-169">El miembro de **datos** es un **GUID** que indica la personalidad del nuevo plan de energía activo.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="b4a6e-170">**GUID \_ de \_ \_ Ahorro de energía mínimo** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span><span class="sxs-lookup"><span data-stu-id="b4a6e-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="b4a6e-171">Alto rendimiento: el esquema está diseñado para ofrecer el máximo rendimiento a costa del ahorro en el consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="b4a6e-172">**GUID \_ de \_ \_ Ahorro de energía máximo** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="b4a6e-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="b4a6e-173">Economizador de energía: el esquema está diseñado para ofrecer el máximo ahorro de consumo de energía a costa del rendimiento y la capacidad de respuesta del sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="b4a6e-174">**GUID \_ de \_ \_ Ahorro de energía típico** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span><span class="sxs-lookup"><span data-stu-id="b4a6e-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="b4a6e-175">Automático: el esquema está diseñado para equilibrar automáticamente el rendimiento y el ahorro de consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_Estado de \_ visualización de sesión GUID \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="b4a6e-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-178">La presentación asociada a la sesión de la aplicación se ha encendido o apagado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="b4a6e-179">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b4a6e-180">Esta notificación se envía solo a las aplicaciones de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="b4a6e-181">Los servicios y otros programas que se ejecutan en la sesión 0 no reciben esta notificación.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="b4a6e-182">El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-183">0X0: la pantalla está desactivada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-184">0x1: la pantalla está activada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-185">0X2: la pantalla está atenuada.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_presencia de \_ usuario de sesión GUID \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="b4a6e-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-188">El estado de usuario asociado con la sesión de la aplicación ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="b4a6e-189">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta notificación está disponible a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b4a6e-190">Esta notificación se envía solo a las aplicaciones de modo de usuario que se ejecutan en una sesión interactiva.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="b4a6e-191">Los servicios y otros programas que se ejecutan en la sesión 0 deben registrarse para la **\_ \_ \_ presencia de usuario global GUID**.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="b4a6e-192">El miembro de **datos** es un **valor DWORD** con uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-193">**PowerUserPresent** (0): el usuario proporciona la entrada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-194">**PowerUserInactive** (2): el tiempo de espera de la actividad de usuario ha transcurrido sin ninguna interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="b4a6e-195">Todas las aplicaciones que se ejecutan en una sesión interactiva en modo usuario deben usar esta opción.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="b4a6e-196">Cuando las aplicaciones en modo kernel se registran para el estado del monitor, deben usar el estado de presentación de la **\_ consola \_ \_ GUID** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="b4a6e-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_AWAYMODE del sistema GUID \_**</span><span class="sxs-lookup"><span data-stu-id="b4a6e-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a6e-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="b4a6e-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="b4a6e-199">El sistema entra o sale del modo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="b4a6e-200">El miembro de **datos** es un **valor DWORD** que indica el estado del modo de ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="b4a6e-201">0X0: el equipo está saliendo del modo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="b4a6e-202">0x1: el equipo está entrando en modo de ubicación.</span><span class="sxs-lookup"><span data-stu-id="b4a6e-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4a6e-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a6e-203">Requirements</span></span>



| <span data-ttu-id="b4a6e-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a6e-204">Requirement</span></span> | <span data-ttu-id="b4a6e-205">Value</span><span class="sxs-lookup"><span data-stu-id="b4a6e-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a6e-206">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4a6e-206">Header</span></span><br/> | <dl> <span data-ttu-id="b4a6e-207"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a6e-207"><dt>WinNT.h</dt></span></span> </dl> |



 

