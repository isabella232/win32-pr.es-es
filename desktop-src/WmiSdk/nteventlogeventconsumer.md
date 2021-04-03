---
description: La clase NTEventLogEventConsumer registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Clase NTEventLogEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908327"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="fb7a4-103">Clase NTEventLogEventConsumer</span><span class="sxs-lookup"><span data-stu-id="fb7a4-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="fb7a4-104">La clase **NTEventLogEventConsumer** registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="fb7a4-105">Esta clase es uno de los consumidores de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="fb7a4-106">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb7a4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb7a4-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="fb7a4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb7a4-108">Members</span></span>

<span data-ttu-id="fb7a4-109">La clase **NTEventLogEventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb7a4-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="fb7a4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb7a4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb7a4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb7a4-111">Properties</span></span>

<span data-ttu-id="fb7a4-112">La clase **NTEventLogEventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb7a4-113">**Categoría**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-116">Categoría de evento.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-116">Event category.</span></span> <span data-ttu-id="fb7a4-117">Esta información es específica del origen y puede tener cualquier valor.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-118">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-119">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="fb7a4-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-121">Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="fb7a4-122">WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="fb7a4-123">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="fb7a4-124">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-125">**Id. de evento**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-128">Mensaje de evento en el archivo DLL del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-128">Event message in the message DLL.</span></span> <span data-ttu-id="fb7a4-129">Esta propiedad no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-133">Tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-133">Type of event.</span></span> <span data-ttu-id="fb7a4-134">Este parámetro puede tener uno de los valores enumerados en la lista siguiente, que se definen en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="fb7a4-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Registro de eventos \_ CORRECTO** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-136">Evento correcto</span><span class="sxs-lookup"><span data-stu-id="fb7a4-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="fb7a4-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Registro de eventos \_ ERROR \_ TPYE** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-138">Evento de error</span><span class="sxs-lookup"><span data-stu-id="fb7a4-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="fb7a4-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Registro de eventos \_ \_Tipo de advertencia** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-140">Evento de advertencia</span><span class="sxs-lookup"><span data-stu-id="fb7a4-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="fb7a4-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Registro de eventos \_ \_Tipo de información** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-142">Evento de información</span><span class="sxs-lookup"><span data-stu-id="fb7a4-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="fb7a4-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Registro de eventos \_ AUDITORÍA \_ correcta** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-144">Tipo de auditoría Success</span><span class="sxs-lookup"><span data-stu-id="fb7a4-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="fb7a4-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Registro de eventos \_ \_Error de auditoría** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="fb7a4-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="fb7a4-146">Tipo de auditoría de error</span><span class="sxs-lookup"><span data-stu-id="fb7a4-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fb7a4-147">**InsertionStringTemplates**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-148">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-150">Matriz de plantillas de cadena estándar que se utiliza como cadena de inserción para una entrada del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-154">Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="fb7a4-155">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-159">Cola máxima para un consumidor específico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="fb7a4-160">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-161">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-164">Calificadores: [ **clave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="fb7a4-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-165">Nombre único de un consumidor.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-166">**NameOfRawDataProperty**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-169">Nombre de la propiedad de evento que contiene los datos que se van a pasar al parámetro *lpRawData* de la función [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="fb7a4-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-170">**NameOfUserSidProperty**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-173">Nombre de la propiedad de evento que contiene un identificador de seguridad (SID) que se va a pasar al parámetro *lpUserSid* de la función [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="fb7a4-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="fb7a4-174">La propiedad debe ser una matriz de bytes (**Uint8**) o una cadena.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="fb7a4-175">Si es una matriz de bytes, se supone que es un SID.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="fb7a4-176">Si es una cadena, es un SID de cadena que se convierte en un SID.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-177">**NumberOfInsertionStrings**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-178">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-180">Número de elementos de la matriz **InsertionStringTemplates** .</span><span class="sxs-lookup"><span data-stu-id="fb7a4-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="fb7a4-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-184">Nombre del origen donde se encuentra un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-184">Source name where a message is located.</span></span> <span data-ttu-id="fb7a4-185">Se supone que el cliente ha registrado un archivo DLL con los mensajes necesarios.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="fb7a4-186">El valor de este parámetro no debe incluir un signo de dos puntos (:) óptico.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="fb7a4-187">**UNCServerName**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb7a4-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb7a4-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fb7a4-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb7a4-190">Nombre del equipo en el que se va a registrar un evento, o **null** si se va a registrar el evento en un servidor local.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="fb7a4-191">De forma predeterminada, los usuarios autenticados no pueden registrar los eventos en el registro de aplicaciones de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="fb7a4-192">Como resultado, el uso de esta propiedad para especificar un equipo remoto no funcionará.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="fb7a4-193">Para obtener información sobre cómo cambiar la seguridad del registro de eventos, consulte este [artículo de Knowledge Base](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb7a4-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb7a4-194">Remarks</span></span>

<span data-ttu-id="fb7a4-195">La clase **NTEventLogEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="fb7a4-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="fb7a4-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fb7a4-196">Examples</span></span>

<span data-ttu-id="fb7a4-197">Para obtener un ejemplo del uso de **NTEventLogEventConsumer** para crear un consumidor, consulte [registro de eventos de NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="fb7a4-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb7a4-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb7a4-198">Requirements</span></span>



| <span data-ttu-id="fb7a4-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb7a4-199">Requirement</span></span> | <span data-ttu-id="fb7a4-200">Value</span><span class="sxs-lookup"><span data-stu-id="fb7a4-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7a4-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7a4-201">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7a4-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb7a4-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb7a4-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7a4-203">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7a4-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb7a4-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb7a4-205">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fb7a4-205">Namespace</span></span><br/>                | <span data-ttu-id="fb7a4-206">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="fb7a4-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="fb7a4-207">MOF</span><span class="sxs-lookup"><span data-stu-id="fb7a4-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb7a4-208"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a4-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb7a4-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb7a4-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb7a4-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb7a4-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb7a4-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb7a4-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7a4-212">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="fb7a4-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="fb7a4-213">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="fb7a4-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="fb7a4-214">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="fb7a4-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="fb7a4-215">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="fb7a4-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

