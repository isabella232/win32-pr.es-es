---
description: La clase LogFileEventConsumer escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Clase LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696920"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="4a068-103">Clase LogFileEventConsumer</span><span class="sxs-lookup"><span data-stu-id="4a068-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="4a068-104">La clase **LogFileEventConsumer** escribe cadenas personalizadas en un archivo de registro de texto cuando se le entregan eventos.</span><span class="sxs-lookup"><span data-stu-id="4a068-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="4a068-105">Las cadenas se separan mediante secuencias de final de línea.</span><span class="sxs-lookup"><span data-stu-id="4a068-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="4a068-106">Esta clase es uno de los consumidores de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="4a068-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="4a068-107">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a068-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a068-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="4a068-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a068-109">Members</span></span>

<span data-ttu-id="4a068-110">La clase **LogFileEventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a068-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="4a068-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a068-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a068-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a068-112">Properties</span></span>

<span data-ttu-id="4a068-113">La clase **LogFileEventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4a068-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a068-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="4a068-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-115">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="4a068-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4a068-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-117">Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="4a068-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="4a068-118">WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a068-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="4a068-119">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="4a068-120">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a068-121">**Nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="4a068-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4a068-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-124">Nombre de un archivo que incluye la ruta de acceso a la que se anexan las entradas de registro.</span><span class="sxs-lookup"><span data-stu-id="4a068-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="4a068-125">Si el archivo no existe, **LogFileEventConsumer** intenta crearlo.</span><span class="sxs-lookup"><span data-stu-id="4a068-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="4a068-126">Se produce un error en el consumidor cuando la ruta de acceso no existe o cuando el usuario que crea el consumidor no tiene permisos de escritura para el archivo o la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4a068-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="4a068-127">**IsUnicode**</span><span class="sxs-lookup"><span data-stu-id="4a068-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4a068-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-130">Si es **true**, el archivo de registro es un archivo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a068-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="4a068-131">Si es **false**, el archivo de registro es un archivo de texto de código multibyte.</span><span class="sxs-lookup"><span data-stu-id="4a068-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="4a068-132">Si el archivo existe, se omite esta propiedad y se usa la configuración del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="4a068-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="4a068-133">Por ejemplo, si **IsUnicode** es **false**, pero el archivo existente es un archivo Unicode, se usa Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a068-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="4a068-134">Si **IsUnicode** es **true**, pero el archivo es código multibyte, se utiliza código multibyte.</span><span class="sxs-lookup"><span data-stu-id="4a068-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="4a068-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="4a068-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4a068-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-138">Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.</span><span class="sxs-lookup"><span data-stu-id="4a068-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="4a068-139">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a068-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="4a068-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4a068-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-143">Tamaño máximo de un archivo de registro en bytes.</span><span class="sxs-lookup"><span data-stu-id="4a068-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="4a068-144">Si el archivo principal supera su tamaño máximo, el contenido se mueve a un archivo diferente y se vacía el archivo principal.</span><span class="sxs-lookup"><span data-stu-id="4a068-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="4a068-145">Un valor de 0 (cero) significa que no hay límite de tamaño.</span><span class="sxs-lookup"><span data-stu-id="4a068-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="4a068-146">El valor predeterminado es 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="4a068-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="4a068-147">El tamaño del archivo se comprueba antes de una operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="4a068-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="4a068-148">Por lo tanto, puede tener un archivo que sea ligeramente mayor que el límite de tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="4a068-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="4a068-149">La siguiente operación de escritura lo detecta e inicia un nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="4a068-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="4a068-150">En la siguiente lista se identifica la estructura de nomenclatura del archivo de copia de seguridad:</span><span class="sxs-lookup"><span data-stu-id="4a068-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="4a068-151">Si el nombre de archivo original es 8,3, la extensión se sustituye por una cadena con el formato "001", "002", y así sucesivamente por el número más pequeño mayor que todos los números elegidos y usados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4a068-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="4a068-152">Si se usa "999", el número elegido es el número más pequeño que no se usa.</span><span class="sxs-lookup"><span data-stu-id="4a068-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="4a068-153">Si el nombre de archivo original no es 8,3, se anexa al nombre de archivo una cadena con el formato "001", "002", etc.</span><span class="sxs-lookup"><span data-stu-id="4a068-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="4a068-154">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4a068-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4a068-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="4a068-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-156">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a068-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-158">Cola máxima para un consumidor específico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4a068-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="4a068-159">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a068-160">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4a068-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4a068-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a068-163">Calificadores: [ **clave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4a068-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="4a068-164">Nombre único para este consumidor.</span><span class="sxs-lookup"><span data-stu-id="4a068-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="4a068-165">**Texto**</span><span class="sxs-lookup"><span data-stu-id="4a068-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a068-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4a068-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a068-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a068-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a068-168">[Plantilla](using-standard-string-templates.md) de cadena estándar para el texto de una entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="4a068-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a068-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a068-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a068-170">**LogFileEventConsumer** no protege el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="4a068-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="4a068-171">Por lo tanto, cuando configure **LogFileEventConsumer**, es importante especificar un directorio que esté protegido con el nivel que necesite.</span><span class="sxs-lookup"><span data-stu-id="4a068-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="4a068-172">La clase **LogFileEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="4a068-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="4a068-173">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4a068-173">Examples</span></span>

<span data-ttu-id="4a068-174">Para obtener un ejemplo del uso de **LogFileEventConsumer** para crear un consumidor, consulte [escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="4a068-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a068-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a068-175">Requirements</span></span>



| <span data-ttu-id="4a068-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a068-176">Requirement</span></span> | <span data-ttu-id="4a068-177">Value</span><span class="sxs-lookup"><span data-stu-id="4a068-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a068-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a068-178">Minimum supported client</span></span><br/> | <span data-ttu-id="4a068-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a068-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a068-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a068-180">Minimum supported server</span></span><br/> | <span data-ttu-id="4a068-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a068-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a068-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4a068-182">Namespace</span></span><br/>                | <span data-ttu-id="4a068-183">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="4a068-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="4a068-184">MOF</span><span class="sxs-lookup"><span data-stu-id="4a068-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a068-185"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a068-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a068-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a068-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a068-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a068-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a068-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a068-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a068-189">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="4a068-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="4a068-190">Escribir en un archivo de registro basado en un evento</span><span class="sxs-lookup"><span data-stu-id="4a068-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="4a068-191">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="4a068-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="4a068-192">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="4a068-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="4a068-193">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="4a068-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

