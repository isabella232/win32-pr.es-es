---
description: La función AddPrinter (agrega una impresora a la lista de impresoras admitidas para un servidor especificado.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Función AddPrinter ((winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276672"
---
# <a name="addprinter-function"></a><span data-ttu-id="ae767-103">AddPrinter (función)</span><span class="sxs-lookup"><span data-stu-id="ae767-103">AddPrinter function</span></span>

<span data-ttu-id="ae767-104">La función **AddPrinter (** agrega una impresora a la lista de impresoras admitidas para un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="ae767-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae767-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae767-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="ae767-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae767-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae767-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae767-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar la impresora.</span><span class="sxs-lookup"><span data-stu-id="ae767-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="ae767-109">Si esta cadena es **null**, la impresora se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="ae767-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="ae767-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ae767-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae767-111">Versión de la estructura a la que apunta *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="ae767-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="ae767-112">Este valor debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="ae767-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="ae767-113">*pPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae767-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae767-114">Puntero a una estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información sobre la impresora.</span><span class="sxs-lookup"><span data-stu-id="ae767-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="ae767-115">Debe especificar valores no **null** para los miembros **pPrinterName**, **pPortName**, **pDriverName** y **pPrintProcessor** de esta estructura antes de llamar a **AddPrinter (**.</span><span class="sxs-lookup"><span data-stu-id="ae767-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae767-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae767-116">Return value</span></span>

<span data-ttu-id="ae767-117">Si la función se ejecuta correctamente, el valor devuelto es un identificador (no seguro para subprocesos) a un nuevo objeto Printer.</span><span class="sxs-lookup"><span data-stu-id="ae767-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="ae767-118">Cuando haya terminado con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="ae767-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="ae767-119">Si se produce un error en la función, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="ae767-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae767-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae767-120">Remarks</span></span>

<span data-ttu-id="ae767-121">No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="ae767-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="ae767-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ae767-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ae767-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae767-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ae767-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ae767-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ae767-125">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="ae767-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="ae767-126">El identificador devuelto no es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ae767-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="ae767-127">Si los autores de las llamadas necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de la impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="ae767-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="ae767-128">Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ae767-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="ae767-129">A continuación se muestran los miembros de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que se pueden establecer antes de que se llame a la función **AddPrinter (** :</span><span class="sxs-lookup"><span data-stu-id="ae767-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="ae767-130">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="ae767-130">**Attributes**</span></span>
-   <span data-ttu-id="ae767-131">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="ae767-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="ae767-132">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="ae767-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="ae767-133">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="ae767-133">**Priority**</span></span>
-   <span data-ttu-id="ae767-134">**pComment**</span><span class="sxs-lookup"><span data-stu-id="ae767-134">**pComment**</span></span>
-   <span data-ttu-id="ae767-135">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ae767-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="ae767-136">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="ae767-136">**pDatatype**</span></span>
-   <span data-ttu-id="ae767-137">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="ae767-137">**pSepFile**</span></span>
-   <span data-ttu-id="ae767-138">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="ae767-138">**pDevMode**</span></span>
-   <span data-ttu-id="ae767-139">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="ae767-139">**pShareName**</span></span>
-   <span data-ttu-id="ae767-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="ae767-140">**pLocation**</span></span>
-   <span data-ttu-id="ae767-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="ae767-141">**StartTime**</span></span>
-   <span data-ttu-id="ae767-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="ae767-142">**pParameters**</span></span>
-   <span data-ttu-id="ae767-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="ae767-143">**UntilTime**</span></span>

<span data-ttu-id="ae767-144">Los miembros **status**, **cJobs** y **AveragePPM** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) están reservados para su uso por parte de la función [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="ae767-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="ae767-145">No se deben establecer antes de llamar a **AddPrinter (**.</span><span class="sxs-lookup"><span data-stu-id="ae767-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="ae767-146">Si **pSecurityDescriptor** es **null**, el sistema asigna un descriptor de seguridad predeterminado a la impresora.</span><span class="sxs-lookup"><span data-stu-id="ae767-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="ae767-147">El descriptor de seguridad predeterminado tiene los permisos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae767-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="ae767-148">Value</span><span class="sxs-lookup"><span data-stu-id="ae767-148">Value</span></span>                          | <span data-ttu-id="ae767-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae767-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae767-150">Administradores y usuarios avanzados</span><span class="sxs-lookup"><span data-stu-id="ae767-150">Administrators and Power Users</span></span> | <span data-ttu-id="ae767-151">Control total en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="ae767-151">Full control on the print queue.</span></span> <span data-ttu-id="ae767-152">Esto significa que los miembros de estos grupos pueden imprimir, administrar la cola (puede eliminar la cola, cambiar cualquier valor de la cola, incluido el descriptor de seguridad) y administrar los trabajos de impresión de todos los usuarios (eliminar, pausar, reanudar, reiniciar trabajos). Tenga en cuenta que los usuarios avanzados no existen antes de Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="ae767-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="ae767-153">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="ae767-153">Creator/Owner</span></span>                  | <span data-ttu-id="ae767-154">Puede administrar sus propios trabajos.</span><span class="sxs-lookup"><span data-stu-id="ae767-154">Can manage own jobs.</span></span> <span data-ttu-id="ae767-155">Esto significa que el usuario que envía trabajos puede administrar (eliminar, pausar, reanudar o reiniciar) sus propios trabajos.</span><span class="sxs-lookup"><span data-stu-id="ae767-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="ae767-156">Todos</span><span class="sxs-lookup"><span data-stu-id="ae767-156">Everyone</span></span>                       | <span data-ttu-id="ae767-157">Ejecutar y control de lectura estándar.</span><span class="sxs-lookup"><span data-stu-id="ae767-157">Execute and standard read control.</span></span> <span data-ttu-id="ae767-158">Esto significa que los miembros del grupo todos pueden imprimir y leer las propiedades de la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="ae767-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="ae767-159">Después de que una aplicación crea un objeto de impresora con la función **AddPrinter (** , debe utilizar la función [**PrinterProperties**](printerproperties.md) para especificar la configuración correcta para el controlador de impresora asociado al objeto Printer.</span><span class="sxs-lookup"><span data-stu-id="ae767-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="ae767-160">La función **AddPrinter (** devuelve un error si ya existe un objeto de impresora con el mismo nombre, a menos que ese objeto esté marcado como pendiente de eliminación.</span><span class="sxs-lookup"><span data-stu-id="ae767-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="ae767-161">En ese caso, no se elimina la impresora existente y los parámetros de creación de **AddPrinter (** se usan para cambiar la configuración de impresora existente (como si la aplicación hubiera usado la función [**SetPrinter**](setprinter.md) ).</span><span class="sxs-lookup"><span data-stu-id="ae767-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="ae767-162">Utilice la función [**EnumPrintProcessors**](enumprintprocessors.md) para enumerar el conjunto de procesadores de impresión instalado en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ae767-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="ae767-163">Utilice la función [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para enumerar el conjunto de tipos de datos que admite un procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="ae767-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="ae767-164">Utilice la función [**EnumPorts**](enumports.md) para enumerar el conjunto de puertos disponibles.</span><span class="sxs-lookup"><span data-stu-id="ae767-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="ae767-165">Utilice la función [**EnumPrinterDrivers**](enumprinterdrivers.md) para enumerar los controladores de impresora instalados.</span><span class="sxs-lookup"><span data-stu-id="ae767-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="ae767-166">El autor de la llamada de la función **AddPrinter (** debe tener acceso al servidor \_ \_ para administrar el acceso al servidor en el que se va a crear la impresora.</span><span class="sxs-lookup"><span data-stu-id="ae767-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="ae767-167">El identificador devuelto por la función tendrá \_ permiso de \_ acceso a toda la impresora y se puede usar para realizar operaciones administrativas en la impresora.</span><span class="sxs-lookup"><span data-stu-id="ae767-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="ae767-168">Si se pasa a la función **DrvPrinterEvent** la \_ marca de evento de impresora \_ \_ sin marca de \_ IU, el controlador no debe usar una llamada de interfaz de usuario durante **DrvPrinterEvent**.</span><span class="sxs-lookup"><span data-stu-id="ae767-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="ae767-169">Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada **VendorSetup** en el archivo. inf de la impresora o, para Plug and Play dispositivos, el instalador puede usar un Coinstalador específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae767-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="ae767-170">Para obtener más información acerca de **VendorSetup**, vea el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ae767-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="ae767-171">El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se habilita una excepción para el uso compartido de archivos e impresoras al ejecutar **AddPrinter (**.</span><span class="sxs-lookup"><span data-stu-id="ae767-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae767-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae767-172">Requirements</span></span>



| <span data-ttu-id="ae767-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae767-173">Requirement</span></span> | <span data-ttu-id="ae767-174">Value</span><span class="sxs-lookup"><span data-stu-id="ae767-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae767-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae767-175">Minimum supported client</span></span><br/> | <span data-ttu-id="ae767-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae767-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae767-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae767-177">Minimum supported server</span></span><br/> | <span data-ttu-id="ae767-178">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae767-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ae767-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae767-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae767-180"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae767-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ae767-181">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae767-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae767-182"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae767-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ae767-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae767-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae767-184"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ae767-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ae767-185">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ae767-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ae767-186">**AddPrinterW** (Unicode) y **AddPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ae767-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="ae767-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae767-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae767-188">Impresión</span><span class="sxs-lookup"><span data-stu-id="ae767-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ae767-189">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ae767-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ae767-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="ae767-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="ae767-191">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="ae767-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="ae767-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="ae767-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="ae767-193">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ae767-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ae767-194">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="ae767-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="ae767-195">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="ae767-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="ae767-196">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ae767-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ae767-197">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ae767-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ae767-198">**PrinterProperties**</span><span class="sxs-lookup"><span data-stu-id="ae767-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="ae767-199">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ae767-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

