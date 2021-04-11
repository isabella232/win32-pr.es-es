---
description: La clase SMTPEventConsumer envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Clase SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279112"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="97b69-103">Clase SMTPEventConsumer</span><span class="sxs-lookup"><span data-stu-id="97b69-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="97b69-104">La clase **SMTPEventConsumer** envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="97b69-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="97b69-105">Debe existir un servidor SMTP en la red.</span><span class="sxs-lookup"><span data-stu-id="97b69-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="97b69-106">La clase SMTPEventConsumer no admite datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="97b69-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="97b69-107">La codificación del mensaje de correo electrónico debe ser US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="97b69-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="97b69-108">Esta clase es uno de los consumidores de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="97b69-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="97b69-109">Para obtener un ejemplo del uso de **SMTPEventConsumer** para crear un consumidor, consulte [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="97b69-110">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="97b69-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="97b69-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="97b69-112">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="97b69-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b69-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97b69-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="97b69-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="97b69-114">Members</span></span>

<span data-ttu-id="97b69-115">La clase **SMTPEventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97b69-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="97b69-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97b69-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97b69-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97b69-117">Properties</span></span>

<span data-ttu-id="97b69-118">La clase **SMTPEventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="97b69-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97b69-119">**BccLine**</span><span class="sxs-lookup"><span data-stu-id="97b69-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-122">Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia oculta.</span><span class="sxs-lookup"><span data-stu-id="97b69-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="97b69-123">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="97b69-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-124">**CcLine**</span><span class="sxs-lookup"><span data-stu-id="97b69-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-127">Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia carbón.</span><span class="sxs-lookup"><span data-stu-id="97b69-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="97b69-128">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="97b69-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-129">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="97b69-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-130">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="97b69-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="97b69-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-132">Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="97b69-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="97b69-133">WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97b69-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="97b69-134">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="97b69-135">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b69-136">**FromLine**</span><span class="sxs-lookup"><span data-stu-id="97b69-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-139">Desde la línea de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar.</span><span class="sxs-lookup"><span data-stu-id="97b69-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="97b69-140">Si es **null**, una línea de se construye con el formato "WinMgmt@*MachineName*".</span><span class="sxs-lookup"><span data-stu-id="97b69-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="97b69-141">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="97b69-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-142">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="97b69-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="97b69-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-144">Matriz de campos de encabezado que se insertan en un mensaje de correo electrónico sin interpretación.</span><span class="sxs-lookup"><span data-stu-id="97b69-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="97b69-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-148">Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.</span><span class="sxs-lookup"><span data-stu-id="97b69-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="97b69-149">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b69-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="97b69-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97b69-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-153">Cola máxima para un consumidor específico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="97b69-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="97b69-154">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b69-155">**Message**</span><span class="sxs-lookup"><span data-stu-id="97b69-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-158">Plantilla de cadena estándar que contiene el cuerpo de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="97b69-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-159">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="97b69-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97b69-162">Calificadores: [ **clave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="97b69-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="97b69-163">Identificador único para el consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="97b69-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-164">**ReplyToLine**</span><span class="sxs-lookup"><span data-stu-id="97b69-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-167">Línea de respuesta de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar.</span><span class="sxs-lookup"><span data-stu-id="97b69-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="97b69-168">Si es **null**, no se utiliza ninguna línea de respuesta a.</span><span class="sxs-lookup"><span data-stu-id="97b69-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="97b69-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-172">Nombre del servidor SMTP a través del cual se envía un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="97b69-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="97b69-173">Los nombres permitidos son una dirección IP o un nombre DNS o NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="97b69-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="97b69-174">Esta propiedad no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="97b69-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="97b69-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-178">Plantilla de cadena estándar que contiene el asunto de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="97b69-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="97b69-179">**ToLine**</span><span class="sxs-lookup"><span data-stu-id="97b69-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97b69-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="97b69-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97b69-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97b69-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97b69-182">Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar que identifica la ubicación a la que se va a enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="97b69-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="97b69-183">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="97b69-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97b69-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97b69-184">Remarks</span></span>

<span data-ttu-id="97b69-185">La clase SMTPEventConsumer se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="97b69-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="97b69-186">Algunas de las propiedades **ToLine**, **CcLine** o **BccLine** pueden ser **null**, pero no pueden ser todas **nulas**.</span><span class="sxs-lookup"><span data-stu-id="97b69-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="97b69-187">La recepción de un código de retorno de error del servicio SMTP se considera un error.</span><span class="sxs-lookup"><span data-stu-id="97b69-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="97b69-188">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="97b69-188">Examples</span></span>

<span data-ttu-id="97b69-189">Para obtener un ejemplo del uso de **SMTPEventConsumer** para crear un consumidor, consulte [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="97b69-190">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="97b69-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97b69-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97b69-191">Requirements</span></span>



| <span data-ttu-id="97b69-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="97b69-192">Requirement</span></span> | <span data-ttu-id="97b69-193">Value</span><span class="sxs-lookup"><span data-stu-id="97b69-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97b69-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97b69-194">Minimum supported client</span></span><br/> | <span data-ttu-id="97b69-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97b69-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97b69-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97b69-196">Minimum supported server</span></span><br/> | <span data-ttu-id="97b69-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97b69-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97b69-198">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97b69-198">Namespace</span></span><br/>                | <span data-ttu-id="97b69-199">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="97b69-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="97b69-200">MOF</span><span class="sxs-lookup"><span data-stu-id="97b69-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97b69-201"><dt>Smtpcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97b69-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="97b69-202">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97b69-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97b69-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97b69-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b69-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="97b69-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b69-205">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="97b69-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="97b69-206">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="97b69-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="97b69-207">Envío de correo electrónico basado en un evento</span><span class="sxs-lookup"><span data-stu-id="97b69-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="97b69-208">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="97b69-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="97b69-209">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="97b69-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




