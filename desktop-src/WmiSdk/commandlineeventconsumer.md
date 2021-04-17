---
description: La clase CommandLineEventConsumer inicia un proceso arbitrario en el sistema local cuando se le entrega un evento.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Clase CommandLineEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187938"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="c324b-103">Clase CommandLineEventConsumer</span><span class="sxs-lookup"><span data-stu-id="c324b-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="c324b-104">La clase **CommandLineEventConsumer** inicia un proceso arbitrario en el sistema local cuando se le entrega un evento.</span><span class="sxs-lookup"><span data-stu-id="c324b-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="c324b-105">Esta clase es uno de los consumidores de eventos estándar que proporciona WMI.</span><span class="sxs-lookup"><span data-stu-id="c324b-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="c324b-106">Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="c324b-107">Al usar la clase **CommandLineEventConsumer** , proteja el archivo ejecutable que desea iniciar.</span><span class="sxs-lookup"><span data-stu-id="c324b-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="c324b-108">Si el archivo ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso (ACL) segura, un usuario no autorizado puede reemplazar el archivo ejecutable con un archivo ejecutable malintencionado.</span><span class="sxs-lookup"><span data-stu-id="c324b-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="c324b-109">Para obtener más información acerca de las ACL, visite la sección seguridad del kit de desarrollo de software (SDK) de Microsoft Windows y consulte [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="c324b-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c324b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c324b-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="c324b-111">Members</span><span class="sxs-lookup"><span data-stu-id="c324b-111">Members</span></span>

<span data-ttu-id="c324b-112">La clase **CommandLineEventConsumer** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c324b-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="c324b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c324b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c324b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c324b-114">Properties</span></span>

<span data-ttu-id="c324b-115">La clase **CommandLineEventConsumer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c324b-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c324b-116">**CommandLineTemplate**</span><span class="sxs-lookup"><span data-stu-id="c324b-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-119">Plantilla de cadena estándar que especifica el proceso que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="c324b-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="c324b-120">Esta propiedad puede ser **null** y la propiedad **ExecutablePath** se usa como línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="c324b-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-121">**CreateNewConsole**</span><span class="sxs-lookup"><span data-stu-id="c324b-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c324b-124">Not used.</span></span> <span data-ttu-id="c324b-125">Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c324b-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="c324b-126">Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="c324b-127">**CreateNewProcessGroup**</span><span class="sxs-lookup"><span data-stu-id="c324b-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-130">Si es **true**, el nuevo proceso es el proceso raíz de un nuevo grupo de procesos.</span><span class="sxs-lookup"><span data-stu-id="c324b-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="c324b-131">El grupo de procesos incluye todos los procesos que son descendientes de este proceso raíz.</span><span class="sxs-lookup"><span data-stu-id="c324b-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="c324b-132">El identificador de proceso del nuevo grupo de procesos es el mismo que el de este identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="c324b-133">El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa los grupos de procesos para habilitar el envío de una señal CTRL + C o Ctrl + Inter a un grupo de procesos de consola.</span><span class="sxs-lookup"><span data-stu-id="c324b-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-134">**CreateSeparateWowVdm**</span><span class="sxs-lookup"><span data-stu-id="c324b-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-137">Si **es true**, el nuevo proceso se ejecuta en una máquina virtual de dos privada (VDM).</span><span class="sxs-lookup"><span data-stu-id="c324b-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="c324b-138">Esto solo es válido cuando se inicia una aplicación que se ejecuta en un sistema operativo Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c324b-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="c324b-139">Si se establece en **false**, todas las aplicaciones que se ejecutan en un sistema operativo Windows de 16 bits se ejecutan como subprocesos en un solo VDM compartido.</span><span class="sxs-lookup"><span data-stu-id="c324b-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="c324b-140">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="c324b-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-141">**CreateSharedWowVdm**</span><span class="sxs-lookup"><span data-stu-id="c324b-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-144">Si **es true**, el método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ejecuta el nuevo proceso en la máquina virtual dos compartida (VDM).</span><span class="sxs-lookup"><span data-stu-id="c324b-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="c324b-145">Esta propiedad puede invalidar el modificador DefaultSeparateVDM en la sección Windows de Win.ini si se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="c324b-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="c324b-146">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="c324b-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-147">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="c324b-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-148">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="c324b-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c324b-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-150">Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="c324b-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="c324b-151">WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c324b-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="c324b-152">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="c324b-153">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c324b-154">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="c324b-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-157">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c324b-157">Not used.</span></span> <span data-ttu-id="c324b-158">Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c324b-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="c324b-159">Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="c324b-160">**ExecutablePath _s**</span><span class="sxs-lookup"><span data-stu-id="c324b-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-163">Módulo que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="c324b-163">Module to execute.</span></span> <span data-ttu-id="c324b-164">La cadena puede especificar la ruta de acceso completa y el nombre de archivo del módulo que se va a ejecutar, o puede especificar un nombre parcial.</span><span class="sxs-lookup"><span data-stu-id="c324b-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="c324b-165">Si se especifica un nombre parcial, se supone la unidad actual y el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="c324b-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="c324b-166">La propiedad **ExecutablePath** puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c324b-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="c324b-167">En ese caso, el nombre del módulo debe ser el primer token delimitado por espacios en blanco en el valor de la propiedad **CommandLineTemplate** .</span><span class="sxs-lookup"><span data-stu-id="c324b-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="c324b-168">Si usa un nombre de archivo largo que contiene un espacio, use cadenas entre comillas para indicar dónde finaliza el nombre de archivo y los argumentos comienzan a aclarar el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c324b-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="c324b-169">Dado que la propiedad **CommandLineTemplate** puede ser una plantilla en la que se proporciona el módulo que se va a ejecutar mediante una variable, una propiedad **ExecutablePath** **nula** permite que el módulo que se especifica en el parámetro se ejecute y, a continuación, está fuera del control.</span><span class="sxs-lookup"><span data-stu-id="c324b-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="c324b-170">Establezca siempre la propiedad **ExecutablePath** en el registro **CommandLineEventConsumer** para incluir el ejecutable necesario, lo que evita que se sobrescriban los parámetros de eventos.</span><span class="sxs-lookup"><span data-stu-id="c324b-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="c324b-171">Si debe usar una plantilla y una variable para especificar el módulo que se va a ejecutar, tenga cuidado con quién tiene concedido el privilegio de escritura completo en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c324b-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="c324b-172">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="c324b-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-173">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-175">Especifica el texto inicial y los colores de fondo si se crea una nueva ventana de consola en una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="c324b-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="c324b-176">**FillAttributes**</span><span class="sxs-lookup"><span data-stu-id="c324b-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c324b-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c324b-179">Texto inicial y colores de fondo, si se crea una nueva ventana de consola en una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="c324b-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="c324b-180">Esta propiedad se omite en una aplicación GUI.</span><span class="sxs-lookup"><span data-stu-id="c324b-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="c324b-181">El valor puede ser cualquier combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="c324b-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="c324b-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c324b-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-183">primer plano azul</span><span class="sxs-lookup"><span data-stu-id="c324b-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="c324b-184">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="c324b-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-185">primer plano verde</span><span class="sxs-lookup"><span data-stu-id="c324b-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="c324b-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c324b-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-187">primer plano rojo</span><span class="sxs-lookup"><span data-stu-id="c324b-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="c324b-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="c324b-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-189">intensidad de primer plano</span><span class="sxs-lookup"><span data-stu-id="c324b-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="c324b-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="c324b-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-191">Fondo azul</span><span class="sxs-lookup"><span data-stu-id="c324b-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="c324b-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c324b-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-193">fondo verde</span><span class="sxs-lookup"><span data-stu-id="c324b-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="c324b-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="c324b-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-195">fondo rojo</span><span class="sxs-lookup"><span data-stu-id="c324b-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="c324b-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="c324b-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-197">intensidad de fondo</span><span class="sxs-lookup"><span data-stu-id="c324b-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="c324b-198">Por ejemplo, las siguientes combinaciones producen texto rojo en un fondo blanco:</span><span class="sxs-lookup"><span data-stu-id="c324b-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="c324b-199">or</span><span class="sxs-lookup"><span data-stu-id="c324b-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="c324b-200">**ForceOffFeedback**</span><span class="sxs-lookup"><span data-stu-id="c324b-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-201">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-203">Si es **true**, se fuerza el cursor de comentarios mientras se inicia el proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="c324b-204">Se muestra el cursor normal.</span><span class="sxs-lookup"><span data-stu-id="c324b-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-205">**ForceOnFeedback**</span><span class="sxs-lookup"><span data-stu-id="c324b-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-206">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-208">Si es **true**, el cursor está en modo de comentarios durante dos segundos después de que se llame a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="c324b-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="c324b-209">Durante esos dos segundos, si el proceso realiza la primera llamada a la interfaz gráfica de usuario, el sistema proporciona cinco segundos más al proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="c324b-210">Durante esos cinco segundos, si el proceso muestra una ventana, el sistema proporciona otros cinco segundos al proceso para terminar de dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="c324b-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-211">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="c324b-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-212">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-214">Número, en segundos, que el servicio WMI espera antes de que se elimine un proceso 0 (cero) indica que no se va a eliminar un proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="c324b-215">El sacrificio de un proceso impide que un proceso se ejecute indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="c324b-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="c324b-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-219">Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.</span><span class="sxs-lookup"><span data-stu-id="c324b-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="c324b-220">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c324b-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="c324b-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-222">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-224">Cola máxima para un consumidor específico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c324b-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="c324b-225">Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c324b-226">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c324b-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c324b-229">Calificadores: [ **clave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c324b-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="c324b-230">Nombre único de un consumidor.</span><span class="sxs-lookup"><span data-stu-id="c324b-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-231">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="c324b-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-232">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c324b-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-234">Nivel de prioridad de programación de los subprocesos del proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="c324b-235">En la lista siguiente se enumeran los niveles de prioridad disponibles.</span><span class="sxs-lookup"><span data-stu-id="c324b-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="c324b-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c324b-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-237">Indica un proceso normal sin necesidad de programar.</span><span class="sxs-lookup"><span data-stu-id="c324b-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="c324b-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-239">Indica un proceso cuyos subprocesos se ejecutan solo cuando el sistema está inactivo y son retenidos por los subprocesos de cualquier proceso que se ejecute en una clase de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="c324b-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="c324b-240">Un ejemplo es un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c324b-240">An example is a screen saver.</span></span> <span data-ttu-id="c324b-241">Los procesos secundarios heredan la clase de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="c324b-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="c324b-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-243">Indica un proceso que realiza tareas críticas en el tiempo de alta prioridad.</span><span class="sxs-lookup"><span data-stu-id="c324b-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="c324b-244">Los subprocesos de un proceso de clase de prioridad alta se adelantan a los subprocesos de procesos de clase de prioridad normal o de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="c324b-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="c324b-245">Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema.</span><span class="sxs-lookup"><span data-stu-id="c324b-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="c324b-246">Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación enlazada a la CPU con una clase de prioridad alta puede usar casi todos los ciclos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c324b-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="c324b-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="c324b-248">Indica un proceso que tiene la prioridad más alta posible.</span><span class="sxs-lookup"><span data-stu-id="c324b-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="c324b-249">Los subprocesos de un proceso de clase de prioridad en tiempo real tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes.</span><span class="sxs-lookup"><span data-stu-id="c324b-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="c324b-250">Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo breve puede hacer que las cachés del disco no se vacíen o hacer que el mouse deje de responder.</span><span class="sxs-lookup"><span data-stu-id="c324b-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c324b-251">**RunInteractively**</span><span class="sxs-lookup"><span data-stu-id="c324b-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-252">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-254">Si es **true**, el proceso se inicia en la estación de inicio interactiva.</span><span class="sxs-lookup"><span data-stu-id="c324b-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="c324b-255">Si es **false**, el proceso se inicia en la estación de servicio predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c324b-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="c324b-256">Esta propiedad invalida la propiedad **DesktopName** .</span><span class="sxs-lookup"><span data-stu-id="c324b-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="c324b-257">Esta propiedad solo se usa localmente y solo si el usuario interactivo es el mismo usuario que configura el consumidor.</span><span class="sxs-lookup"><span data-stu-id="c324b-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="c324b-258">A partir de Windows Vista, el proceso que ejecuta la instancia de **CommandLineEventConsumer** se inicia con la cuenta **LocalSystem** y se encuentra en la sesión 0.</span><span class="sxs-lookup"><span data-stu-id="c324b-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="c324b-259">Los servicios que se ejecutan en la sesión 0 no pueden interactuar con las sesiones de usuario.</span><span class="sxs-lookup"><span data-stu-id="c324b-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-260">**ShowWindowCommand**</span><span class="sxs-lookup"><span data-stu-id="c324b-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-261">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-263">Estado de la ventana Mostrar.</span><span class="sxs-lookup"><span data-stu-id="c324b-263">Window show state.</span></span> <span data-ttu-id="c324b-264">Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la función [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="c324b-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-265">**UseDefaultErrorMode**</span><span class="sxs-lookup"><span data-stu-id="c324b-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-266">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c324b-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-268">Si es **true**, se usa el modo de error predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c324b-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="c324b-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-272">Título que aparece en la barra de título del proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="c324b-273">Esta propiedad se omite para las aplicaciones GUI.</span><span class="sxs-lookup"><span data-stu-id="c324b-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="c324b-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c324b-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-277">Directorio de trabajo de este proceso.</span><span class="sxs-lookup"><span data-stu-id="c324b-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-278">**XCoordinate**</span><span class="sxs-lookup"><span data-stu-id="c324b-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-279">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-281">Desplazamiento X, en píxeles, desde el borde izquierdo de la pantalla hasta el borde izquierdo de la ventana, si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c324b-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-282">**XNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="c324b-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-285">Ancho del búfer de pantalla, en columnas de caracteres, si se crea una nueva ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="c324b-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="c324b-286">Esta propiedad se omite en un proceso de GUI.</span><span class="sxs-lookup"><span data-stu-id="c324b-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-287">**XSize**</span><span class="sxs-lookup"><span data-stu-id="c324b-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-288">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-290">Ancho, en píxeles, de una nueva ventana, si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c324b-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-291">**YCoordinate**</span><span class="sxs-lookup"><span data-stu-id="c324b-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-294">Desplazamiento y, en píxeles, desde el borde superior de la pantalla hasta el borde superior de la ventana, si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c324b-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-295">**YNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="c324b-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-296">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-298">Alto del búfer de pantalla, en filas de caracteres, si se crea una nueva ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="c324b-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="c324b-299">Esta propiedad se omite en un proceso de GUI.</span><span class="sxs-lookup"><span data-stu-id="c324b-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="c324b-300">**YSize**</span><span class="sxs-lookup"><span data-stu-id="c324b-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c324b-301">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c324b-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c324b-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c324b-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c324b-303">Alto, en píxeles, de la nueva ventana, si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c324b-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c324b-304">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c324b-304">Remarks</span></span>

<span data-ttu-id="c324b-305">La clase **CommandLineEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="c324b-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="c324b-306">La propiedad **CreateSeparateWowVdm** indica si el nuevo proceso se ejecuta en una máquina virtual de dos privada (VDM).</span><span class="sxs-lookup"><span data-stu-id="c324b-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="c324b-307">La ventaja de ejecutarse por separado es que un bloqueo solo finaliza el VDM único.</span><span class="sxs-lookup"><span data-stu-id="c324b-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="c324b-308">Los programas que se ejecutan en VDMs DISTINCT continúan funcionando con normalidad y las aplicaciones de 16 bits basadas en Windows que se ejecutan en VDMs independientes tienen colas de entrada independientes.</span><span class="sxs-lookup"><span data-stu-id="c324b-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="c324b-309">Esto significa que si una aplicación deja de responder momentáneamente, las aplicaciones en VDMs independientes continúan recibiendo la entrada.</span><span class="sxs-lookup"><span data-stu-id="c324b-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="c324b-310">El inconveniente de ejecutarse por separado es que requiere mucho más memoria para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="c324b-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="c324b-311">Debe establecer esta propiedad en **true** solo si el usuario solicita que las aplicaciones basadas en Windows de 16 bits se ejecuten en su propio VDM.</span><span class="sxs-lookup"><span data-stu-id="c324b-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="c324b-312">**CommandLineEventConsumer** usa el método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) internamente y pasa las propiedades **ExecutablePath** y **CommandLineTemplate** como parámetros *lpApplicationName* y *lpCommandLine* .</span><span class="sxs-lookup"><span data-stu-id="c324b-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="c324b-313">En el siguiente ejemplo de código de Managed Object Format (MOF) no se usa correctamente **CommandLineEventConsumer** .</span><span class="sxs-lookup"><span data-stu-id="c324b-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="c324b-314">El método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pasa *lpCommandLine* como `argv[0]` , `argv[1]` , etc.</span><span class="sxs-lookup"><span data-stu-id="c324b-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="c324b-315">Como en el `argv[0]` caso de las aplicaciones de 16 bits que se han reservado para el nombre del archivo ejecutable, el código MOF anterior hace que el proceso se cree como si se escribiera el siguiente comando en el símbolo del sistema: **c: \\ Windows \\ system32 \\cscript.exe parám1 param2**.</span><span class="sxs-lookup"><span data-stu-id="c324b-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="c324b-316">El comando anterior no se ejecuta correctamente porque Cscript.exe no examina `argv[0]` , por lo que no reconoce que no contenga su propio nombre, sino algo más ("c: \\ \\ scripts \\ \\MyScript.js").</span><span class="sxs-lookup"><span data-stu-id="c324b-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="c324b-317">En el ejemplo siguiente se identifica el uso recomendado de **CommandLineEventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="c324b-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="c324b-318">El uso anterior de **CommandLineEventConsumer** da como resultado el proceso creado como si se escribiera el siguiente comando en el símbolo del sistema: **c: \\ Windows \\ system32 \\cscript.exe c: \\ scripts \\MyScript.js parám1 parám2**</span><span class="sxs-lookup"><span data-stu-id="c324b-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="c324b-319">Como "c: \\ \\ scripts \\ \\MyScript.js" es ahora `argv[1]` , lo verán Cscript.exe y el comando se ejecutará correctamente.</span><span class="sxs-lookup"><span data-stu-id="c324b-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="c324b-320">Para obtener más información, vea la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="c324b-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="c324b-321">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c324b-321">Examples</span></span>

<span data-ttu-id="c324b-322">Para obtener un ejemplo del uso de **CommandLineEventConsumer** para crear un consumidor, vea [ejecutar un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c324b-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c324b-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c324b-323">Requirements</span></span>



| <span data-ttu-id="c324b-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="c324b-324">Requirement</span></span> | <span data-ttu-id="c324b-325">Value</span><span class="sxs-lookup"><span data-stu-id="c324b-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c324b-326">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c324b-326">Minimum supported client</span></span><br/> | <span data-ttu-id="c324b-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c324b-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c324b-328">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c324b-328">Minimum supported server</span></span><br/> | <span data-ttu-id="c324b-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c324b-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c324b-330">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c324b-330">Namespace</span></span><br/>                | <span data-ttu-id="c324b-331">\\Suscripción raíz</span><span class="sxs-lookup"><span data-stu-id="c324b-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="c324b-332">MOF</span><span class="sxs-lookup"><span data-stu-id="c324b-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c324b-333"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c324b-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="c324b-334">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c324b-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c324b-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c324b-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c324b-336">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c324b-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c324b-337">Clases de consumidor estándar</span><span class="sxs-lookup"><span data-stu-id="c324b-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="c324b-338">Supervisión y respuesta a eventos con consumidores estándar</span><span class="sxs-lookup"><span data-stu-id="c324b-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="c324b-339">Crear un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="c324b-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="c324b-340">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="c324b-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="c324b-341">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="c324b-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

