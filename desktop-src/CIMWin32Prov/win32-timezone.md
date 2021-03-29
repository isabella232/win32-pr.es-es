---
description: La \_ zona horaria de Win32&\# 8194; La clase WMI representa la información de zona horaria de un equipo que ejecuta Windows, que incluye los cambios necesarios para realizar la transición a la transición del horario de verano.
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907174"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="692c3-103">\_Clase TimeZone de Win32</span><span class="sxs-lookup"><span data-stu-id="692c3-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="692c3-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ TimeZone de Win32** representa la información de zona horaria de un equipo que ejecuta Windows, que incluye los cambios necesarios para realizar la transición a la transición del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="692c3-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="692c3-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="692c3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="692c3-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="692c3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="692c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="692c3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="692c3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="692c3-108">Members</span></span>

<span data-ttu-id="692c3-109">La **clase \_ TimeZone de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="692c3-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="692c3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="692c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="692c3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="692c3-111">Properties</span></span>

<span data-ttu-id="692c3-112">La **clase \_ TimeZone de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="692c3-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="692c3-113">**Sesgo**</span><span class="sxs-lookup"><span data-stu-id="692c3-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-114">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="692c3-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| de hora estructuras de tiempo de la \| [**\_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="692c3-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-117">Diferencia actual para la conversión de hora local.</span><span class="sxs-lookup"><span data-stu-id="692c3-117">Current bias for local time translation.</span></span> <span data-ttu-id="692c3-118">La diferencia es la diferencia entre la hora universal coordinada (UTC) y la hora local.</span><span class="sxs-lookup"><span data-stu-id="692c3-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="692c3-119">Todas las traducciones entre la hora UTC y la hora local se basan en la siguiente fórmula: UTC = hora local-diferencia.</span><span class="sxs-lookup"><span data-stu-id="692c3-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="692c3-120">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="692c3-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="692c3-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="692c3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-124">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="692c3-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="692c3-125">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="692c3-125">Short textual description of the current object.</span></span>

<span data-ttu-id="692c3-126">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="692c3-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="692c3-127">**DaylightBias**</span><span class="sxs-lookup"><span data-stu-id="692c3-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="692c3-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-130">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Structures Time \| [**\_ \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information). \| DaylightBias"), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="692c3-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-131">Valor de diferencia que se va a usar durante las traducciones de hora local que se producen durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="692c3-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="692c3-132">Esta propiedad se omite si no se proporciona un valor para la propiedad **DaylightDay** .</span><span class="sxs-lookup"><span data-stu-id="692c3-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="692c3-133">El valor de esta propiedad se agrega a la propiedad **Bias** para formar la diferencia usada durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="692c3-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="692c3-134">En la mayoría de las zonas horarias, el valor de esta propiedad es-60.</span><span class="sxs-lookup"><span data-stu-id="692c3-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="692c3-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-136">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-138">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="692c3-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-139">**DaylightDayOfWeek** de **DaylightMonth** cuando se produce la transición desde el horario estándar al horario de verano en este sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="692c3-140">Ejemplo: Si el día de la transición (**DaylightDayOfWeek**) se produce en domingo, el valor "1" indica el primer domingo del **DaylightMonth**, "2" indica el segundo domingo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="692c3-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="692c3-141">El valor "5" indica el último **DaylightDayOfWeek** del mes.</span><span class="sxs-lookup"><span data-stu-id="692c3-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-142">**DaylightDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="692c3-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-143">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="692c3-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-145">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="692c3-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-146">Día de la semana en que se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="692c3-147">**Domingo** (0)</span><span class="sxs-lookup"><span data-stu-id="692c3-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="692c3-148">**Lunes** (1)</span><span class="sxs-lookup"><span data-stu-id="692c3-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="692c3-149">**Martes** (2)</span><span class="sxs-lookup"><span data-stu-id="692c3-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="692c3-150">**Miércoles** (3)</span><span class="sxs-lookup"><span data-stu-id="692c3-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="692c3-151">**Jueves** (4)</span><span class="sxs-lookup"><span data-stu-id="692c3-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="692c3-152">**Viernes** (5)</span><span class="sxs-lookup"><span data-stu-id="692c3-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="692c3-153">**Sábado** (6)</span><span class="sxs-lookup"><span data-stu-id="692c3-153">**Saturday** (6)</span></span>


<span data-ttu-id="692c3-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="692c3-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="692c3-155">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="692c3-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="692c3-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="692c3-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-159">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="692c3-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-160">Hora del día en que se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-161">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="692c3-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="692c3-162">**DaylightMillisecond**</span><span class="sxs-lookup"><span data-stu-id="692c3-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-165">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="692c3-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-166">Milisegundo de **DaylightSecond** cuando se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="692c3-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-170">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="692c3-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-171">Minuto de **DaylightHour** cuando se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-172">Ejemplo: 59</span><span class="sxs-lookup"><span data-stu-id="692c3-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="692c3-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="692c3-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-176">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="692c3-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-177">Mes en el que se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="692c3-178">**Enero** (1)</span><span class="sxs-lookup"><span data-stu-id="692c3-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="692c3-179">**Febrero** (2)</span><span class="sxs-lookup"><span data-stu-id="692c3-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="692c3-180">**Marzo** (3)</span><span class="sxs-lookup"><span data-stu-id="692c3-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="692c3-181">**Abril** (4)</span><span class="sxs-lookup"><span data-stu-id="692c3-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="692c3-182">**Mayo** (5)</span><span class="sxs-lookup"><span data-stu-id="692c3-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="692c3-183">**Junio** (6)</span><span class="sxs-lookup"><span data-stu-id="692c3-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="692c3-184">**Julio** (7)</span><span class="sxs-lookup"><span data-stu-id="692c3-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="692c3-185">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="692c3-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="692c3-186">**Septiembre** (9)</span><span class="sxs-lookup"><span data-stu-id="692c3-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="692c3-187">**Octubre** (10)</span><span class="sxs-lookup"><span data-stu-id="692c3-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="692c3-188">**Noviembre** (11)</span><span class="sxs-lookup"><span data-stu-id="692c3-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="692c3-189">**Diciembre** (12)</span><span class="sxs-lookup"><span data-stu-id="692c3-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="692c3-190">**DaylightName**</span><span class="sxs-lookup"><span data-stu-id="692c3-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="692c3-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-193">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Structures \| [**\_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName")</span><span class="sxs-lookup"><span data-stu-id="692c3-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-194">Zona horaria que se representa cuando el horario de verano está en vigor.</span><span class="sxs-lookup"><span data-stu-id="692c3-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="692c3-195">Ejemplo: "EDT" (horario de verano oriental)</span><span class="sxs-lookup"><span data-stu-id="692c3-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="692c3-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="692c3-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-199">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="692c3-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-200">Segundo de **DaylightMinute** cuando se produce la transición desde el horario estándar al horario de verano en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-201">Ejemplo: 59</span><span class="sxs-lookup"><span data-stu-id="692c3-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="692c3-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="692c3-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-205">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="692c3-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-206">Año en vigor el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="692c3-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="692c3-207">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="692c3-207">This property is not required.</span></span>

<span data-ttu-id="692c3-208">Ejemplo: 1997</span><span class="sxs-lookup"><span data-stu-id="692c3-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="692c3-209">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="692c3-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="692c3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="692c3-212">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="692c3-212">Textual description of the current object.</span></span>

<span data-ttu-id="692c3-213">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="692c3-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="692c3-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="692c3-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="692c3-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-217">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="692c3-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="692c3-218">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="692c3-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="692c3-219">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="692c3-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="692c3-220">**StandardBias**</span><span class="sxs-lookup"><span data-stu-id="692c3-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-221">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-223">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Structures Time \| [**\_ \_ Information**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="692c3-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-224">Valor de diferencia que se usa cuando el horario de verano no está en vigor.</span><span class="sxs-lookup"><span data-stu-id="692c3-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="692c3-225">Esta propiedad se omite si no se proporciona un valor para **StandardDay** .</span><span class="sxs-lookup"><span data-stu-id="692c3-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="692c3-226">El valor de esta propiedad se agrega a la propiedad **Bias** para formar la diferencia durante el horario estándar.</span><span class="sxs-lookup"><span data-stu-id="692c3-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="692c3-227">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="692c3-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="692c3-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="692c3-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-229">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-231">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDay")</span><span class="sxs-lookup"><span data-stu-id="692c3-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-232">**StandardDayOfWeek** de **StandardMonth** cuando se produce la transición del horario de verano al horario estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-233">Si el día de la transición (**StandardDayOfWeek**) se produce en domingo, el valor "1" indica el primer domingo del **StandardMonth**, "2" indica el segundo domingo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="692c3-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="692c3-234">El valor "5" indica el último **StandardDayOfWeek** del mes.</span><span class="sxs-lookup"><span data-stu-id="692c3-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-235">**StandardDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="692c3-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-236">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="692c3-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-238">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wDayOfWeek")</span><span class="sxs-lookup"><span data-stu-id="692c3-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-239">Día de la semana en que se produce la transición del horario de verano a la hora estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="692c3-240">**Domingo** (0)</span><span class="sxs-lookup"><span data-stu-id="692c3-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="692c3-241">**Lunes** (1)</span><span class="sxs-lookup"><span data-stu-id="692c3-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="692c3-242">**Martes** (2)</span><span class="sxs-lookup"><span data-stu-id="692c3-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="692c3-243">**Miércoles** (3)</span><span class="sxs-lookup"><span data-stu-id="692c3-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="692c3-244">**Jueves** (4)</span><span class="sxs-lookup"><span data-stu-id="692c3-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="692c3-245">**Viernes** (5)</span><span class="sxs-lookup"><span data-stu-id="692c3-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="692c3-246">**Sábado** (6)</span><span class="sxs-lookup"><span data-stu-id="692c3-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="692c3-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="692c3-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-248">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-250">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wHour")</span><span class="sxs-lookup"><span data-stu-id="692c3-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-251">Hora del día en que se produce la transición del horario de verano a la hora estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-252">Ejemplo: 11</span><span class="sxs-lookup"><span data-stu-id="692c3-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="692c3-253">**StandardMillisecond**</span><span class="sxs-lookup"><span data-stu-id="692c3-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-254">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-256">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMilliseconds")</span><span class="sxs-lookup"><span data-stu-id="692c3-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-257">Milisegundo de **StandardSecond** cuando se produce la transición del horario de verano a la hora estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="692c3-258">**StandardMinute**</span><span class="sxs-lookup"><span data-stu-id="692c3-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-259">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-261">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMinute")</span><span class="sxs-lookup"><span data-stu-id="692c3-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-262">Minuto de **StandardDay** cuando se produce la transición del horario de verano al horario estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-263">Ejemplo: 59</span><span class="sxs-lookup"><span data-stu-id="692c3-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="692c3-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="692c3-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-265">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-267">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wMonth")</span><span class="sxs-lookup"><span data-stu-id="692c3-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-268">Mes en que se produce la transición del horario de verano al horario estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="692c3-269">**Enero** (1)</span><span class="sxs-lookup"><span data-stu-id="692c3-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="692c3-270">**Febrero** (2)</span><span class="sxs-lookup"><span data-stu-id="692c3-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="692c3-271">**Marzo** (3)</span><span class="sxs-lookup"><span data-stu-id="692c3-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="692c3-272">**Abril** (4)</span><span class="sxs-lookup"><span data-stu-id="692c3-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="692c3-273">**Mayo** (5)</span><span class="sxs-lookup"><span data-stu-id="692c3-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="692c3-274">**Junio** (6)</span><span class="sxs-lookup"><span data-stu-id="692c3-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="692c3-275">**Julio** (7)</span><span class="sxs-lookup"><span data-stu-id="692c3-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="692c3-276">**Agosto** (8)</span><span class="sxs-lookup"><span data-stu-id="692c3-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="692c3-277">**Septiembre** (9)</span><span class="sxs-lookup"><span data-stu-id="692c3-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="692c3-278">**Octubre** (10)</span><span class="sxs-lookup"><span data-stu-id="692c3-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="692c3-279">**Noviembre** (11)</span><span class="sxs-lookup"><span data-stu-id="692c3-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="692c3-280">**Diciembre** (12)</span><span class="sxs-lookup"><span data-stu-id="692c3-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="692c3-281">**StandardName**</span><span class="sxs-lookup"><span data-stu-id="692c3-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="692c3-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-284">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Time Structures \| [**\_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")</span><span class="sxs-lookup"><span data-stu-id="692c3-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-285">Nombre de la zona horaria que se representa cuando está vigente la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="692c3-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="692c3-286">Ejemplo: "EST" (hora estándar del este)</span><span class="sxs-lookup"><span data-stu-id="692c3-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="692c3-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="692c3-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-288">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-290">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wSecond")</span><span class="sxs-lookup"><span data-stu-id="692c3-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-291">Segundo de **StandardMinute** cuando se produce la transición del horario de verano al horario estándar en un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="692c3-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="692c3-292">Ejemplo: 59</span><span class="sxs-lookup"><span data-stu-id="692c3-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="692c3-293">**StandardYear**</span><span class="sxs-lookup"><span data-stu-id="692c3-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="692c3-294">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="692c3-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="692c3-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="692c3-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="692c3-296">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| hora estructuras de tiempo \| [**\_ \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardDate \| wYear")</span><span class="sxs-lookup"><span data-stu-id="692c3-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="692c3-297">Año en el que está vigente la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="692c3-297">Year when standard time is in effect.</span></span> <span data-ttu-id="692c3-298">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="692c3-298">This property is not required.</span></span>

<span data-ttu-id="692c3-299">Ejemplo: 1997</span><span class="sxs-lookup"><span data-stu-id="692c3-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="692c3-300">Observaciones</span><span class="sxs-lookup"><span data-stu-id="692c3-300">Remarks</span></span>

<span data-ttu-id="692c3-301">La **clase \_ TimeZone de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="692c3-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="692c3-302">No puede usar formatos de fecha y hora estándar, como 10/18/2002, al escribir consultas de WMI.</span><span class="sxs-lookup"><span data-stu-id="692c3-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="692c3-303">En su lugar, debe convertir las fechas usadas en las consultas al formato UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="692c3-304">Esto requiere dos pasos: 1) debe determinar el desplazamiento (diferencia en minutos) entre la zona horaria y la hora del meridiano de Greenwich, y 2) debe convertir 10/18/2002 a un valor UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="692c3-305">Determinar el desplazamiento a partir de la hora del meridiano de Greenwich</span><span class="sxs-lookup"><span data-stu-id="692c3-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="692c3-306">De forma no admitida, WMI dificulta el trabajo con fechas y horas. Afortunadamente, WMI facilita la determinación del desplazamiento entre la zona horaria y la hora del meridiano de Greenwich.</span><span class="sxs-lookup"><span data-stu-id="692c3-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="692c3-307">La clase WMI la \_ zona horaria de Win32 incluye una propiedad-Bias, que devuelve el desplazamiento GMT.</span><span class="sxs-lookup"><span data-stu-id="692c3-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="692c3-308">Convertir una fecha en un valor UTC</span><span class="sxs-lookup"><span data-stu-id="692c3-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="692c3-309">Después de determinar el desplazamiento GMT, debe convertir una fecha estándar como 10/18/2002 a una fecha UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="692c3-310">Para convertir una fecha estándar en una fecha UTC, puede usar funciones de fecha de VBScript como Year, month y Day para aislar los componentes individuales que constituyen una fecha UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="692c3-311">Una vez que tenga valores individuales para estos componentes, puede concatenarlos de la misma manera que cualquier otro valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="692c3-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="692c3-312">Las fechas UTC se tratan como cadenas porque el desplazamiento GMT debe anexarse al final.</span><span class="sxs-lookup"><span data-stu-id="692c3-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="692c3-313">Si la fecha se ha detectado como un número, este valor:</span><span class="sxs-lookup"><span data-stu-id="692c3-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="692c3-314">Se trataría erróneamente como una ecuación matemática (paréntesis agregados para mayor claridad):</span><span class="sxs-lookup"><span data-stu-id="692c3-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="692c3-315">Por ejemplo, en la fecha 10/18/2002, los componentes individuales son:</span><span class="sxs-lookup"><span data-stu-id="692c3-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="692c3-316">Año: 2002</span><span class="sxs-lookup"><span data-stu-id="692c3-316">Year: 2002</span></span>
-   <span data-ttu-id="692c3-317">Mes: 10</span><span class="sxs-lookup"><span data-stu-id="692c3-317">Month: 10</span></span>
-   <span data-ttu-id="692c3-318">Día: 18</span><span class="sxs-lookup"><span data-stu-id="692c3-318">Day: 18</span></span>

<span data-ttu-id="692c3-319">El script necesitaría combinar estos tres valores: la cadena "113047,000000" (que representa la hora, incluidos los milisegundos) y el desplazamiento GMT para derivar una fecha UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="692c3-320">Por ejemplo, (se han agregado paréntesis de nuevo para mayor claridad):</span><span class="sxs-lookup"><span data-stu-id="692c3-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="692c3-321">Puede usar las funciones de VBScript hour, Minute y Second para convertir la parte de hora de una fecha UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="692c3-322">Por lo tanto, una hora como 11:30:47 A.M.</span><span class="sxs-lookup"><span data-stu-id="692c3-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="692c3-323">se convertiría en 113047.</span><span class="sxs-lookup"><span data-stu-id="692c3-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="692c3-324">Hay un factor complicado.</span><span class="sxs-lookup"><span data-stu-id="692c3-324">There is one complicating factor.</span></span> <span data-ttu-id="692c3-325">El mes debe ocupar las posiciones 5 y 6 en la cadena; el día debe ocupar las posiciones 7 y 8.</span><span class="sxs-lookup"><span data-stu-id="692c3-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="692c3-326">Esto no es un problema con el mes 10 y el día 18.</span><span class="sxs-lookup"><span data-stu-id="692c3-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="692c3-327">Pero, ¿cómo se obtiene el 5 de julio (mes 7, día 5) para rellenar las posiciones necesarias?</span><span class="sxs-lookup"><span data-stu-id="692c3-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="692c3-328">La respuesta es agregar un cero inicial a cada valor, cambiando de 7 a 07 y del 5 al 05.</span><span class="sxs-lookup"><span data-stu-id="692c3-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="692c3-329">Para ello, utilice la función Len de VBScript para comprobar la longitud (número de caracteres) del mes y el día.</span><span class="sxs-lookup"><span data-stu-id="692c3-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="692c3-330">Si la longitud es 1 (lo que significa que solo hay un carácter), agregue un cero a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="692c3-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="692c3-331">Modo</span><span class="sxs-lookup"><span data-stu-id="692c3-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="692c3-332">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="692c3-332">Examples</span></span>

<span data-ttu-id="692c3-333">En el siguiente ejemplo de VBScript se convierte la fecha actual en una fecha UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="692c3-334">El siguiente código de VBScript sampledetermines el desplazamiento GMT y, a continuación, convierte una fecha actual especificada (en este caso, 10/18/2002) en el formato de fecha y hora UTC.</span><span class="sxs-lookup"><span data-stu-id="692c3-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="692c3-335">Una vez convertida la fecha, ese valor se utiliza para buscar en un equipo y devuelve una lista de todas las carpetas que se crearon después de 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="692c3-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="692c3-336">En el ejemplo de código de VBScript siguiente se muestra la configuración de \_ las instancias de zona horaria de Win32.</span><span class="sxs-lookup"><span data-stu-id="692c3-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="692c3-337">Requisitos</span><span class="sxs-lookup"><span data-stu-id="692c3-337">Requirements</span></span>



| <span data-ttu-id="692c3-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="692c3-338">Requirement</span></span> | <span data-ttu-id="692c3-339">Value</span><span class="sxs-lookup"><span data-stu-id="692c3-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="692c3-340">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="692c3-340">Minimum supported client</span></span><br/> | <span data-ttu-id="692c3-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="692c3-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="692c3-342">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="692c3-342">Minimum supported server</span></span><br/> | <span data-ttu-id="692c3-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="692c3-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="692c3-344">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="692c3-344">Namespace</span></span><br/>                | <span data-ttu-id="692c3-345">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="692c3-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="692c3-346">MOF</span><span class="sxs-lookup"><span data-stu-id="692c3-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="692c3-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="692c3-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="692c3-348">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="692c3-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="692c3-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="692c3-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="692c3-350">Vea también</span><span class="sxs-lookup"><span data-stu-id="692c3-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692c3-351">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="692c3-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="692c3-352">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="692c3-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="692c3-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="692c3-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="692c3-354">Formato de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="692c3-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="692c3-355">Tareas de WMI: fechas y horas</span><span class="sxs-lookup"><span data-stu-id="692c3-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
