---
description: Lee datos de un archivo abierto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Función NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538535"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="82d92-103">NtReadFile función)</span><span class="sxs-lookup"><span data-stu-id="82d92-103">NtReadFile function</span></span>

<span data-ttu-id="82d92-104">Lee datos de un archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="82d92-104">Reads data from an open file.</span></span>

<span data-ttu-id="82d92-105">Esta función es el modo de usuario equivalente a la función [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentada en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="82d92-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="82d92-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82d92-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="82d92-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82d92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d92-108">*FileHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d92-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-109">Identificador del objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="82d92-109">Handle to the file object.</span></span> <span data-ttu-id="82d92-110">Este identificador se crea mediante una llamada correcta a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) o [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span><span class="sxs-lookup"><span data-stu-id="82d92-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="82d92-111">*Evento* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="82d92-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-112">Opcionalmente, identificador de un objeto de evento que se va a establecer en el estado señalado una vez finalizada la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="82d92-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="82d92-113">Los controladores intermedios y de dispositivo deben establecer este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="82d92-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-114">*ApcRoutine* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="82d92-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-115">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="82d92-115">This parameter is reserved.</span></span> <span data-ttu-id="82d92-116">Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.</span><span class="sxs-lookup"><span data-stu-id="82d92-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-117">*ApcContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="82d92-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-118">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="82d92-118">This parameter is reserved.</span></span> <span data-ttu-id="82d92-119">Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.</span><span class="sxs-lookup"><span data-stu-id="82d92-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-120">*IoStatusBlock* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82d92-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-121">Puntero a una estructura de [**\_ \_ bloque de estado de e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) que recibe el estado final de finalización e información sobre la operación de lectura solicitada.</span><span class="sxs-lookup"><span data-stu-id="82d92-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="82d92-122">El miembro de **información** recibe el número de bytes realmente leídos del archivo.</span><span class="sxs-lookup"><span data-stu-id="82d92-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-123">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82d92-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-124">Puntero a un búfer asignado por el llamador que recibe los datos leídos del archivo.</span><span class="sxs-lookup"><span data-stu-id="82d92-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-125">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82d92-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-126">Tamaño, en bytes, del búfer al que apunta el *búfer*.</span><span class="sxs-lookup"><span data-stu-id="82d92-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-127">*Byteoffset (* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="82d92-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-128">Puntero a una variable que especifica el desplazamiento de bytes de inicio en el archivo donde comenzará la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="82d92-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="82d92-129">Si se intenta leer más allá del final del archivo, **NtReadFile** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="82d92-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="82d92-130">Si la llamada a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece una de las alertas de e/s sincrónicas sincrónicas del archivo de marcas de *CreateOptions* o del archivo \_ \_ \_ \_ \_ \_ , el administrador de e/s mantiene la posición actual del archivo.</span><span class="sxs-lookup"><span data-stu-id="82d92-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="82d92-131">Si es así, el llamador de **NtReadFile** puede especificar que se use el desplazamiento de la posición del archivo actual en lugar de un valor *byteoffset (* explícito.</span><span class="sxs-lookup"><span data-stu-id="82d92-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="82d92-132">Esta especificación puede realizarse mediante uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="82d92-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="82d92-133">Especifique un puntero a un **valor \_ entero grande** con el miembro **HighPart** establecido en-1 y el miembro **LowPart** establecido en el archivo de valor definido por el sistema \_ use la posición del puntero de \_ archivo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="82d92-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="82d92-134">Pase un puntero **nulo** para *byteoffset (*.</span><span class="sxs-lookup"><span data-stu-id="82d92-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="82d92-135">**NtReadFile** actualiza la posición del archivo actual agregando el número de bytes leídos cuando finaliza la operación de lectura, si usa la posición de archivo actual que mantiene el administrador de e/s.</span><span class="sxs-lookup"><span data-stu-id="82d92-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="82d92-136">Incluso cuando el administrador de e/s mantiene la posición actual del archivo, el autor de la llamada puede restablecer esta posición pasando un valor de *byteoffset (* explícito a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="82d92-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="82d92-137">Al hacerlo, se cambia automáticamente la posición del archivo actual a ese valor *byteoffset (* , se realiza la operación de lectura y, a continuación, se actualiza la posición según el número de bytes leídos realmente.</span><span class="sxs-lookup"><span data-stu-id="82d92-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="82d92-138">Esta técnica proporciona el servicio de búsqueda y lectura atómica del llamador.</span><span class="sxs-lookup"><span data-stu-id="82d92-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="82d92-139">*Clave* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="82d92-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d92-140">Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.</span><span class="sxs-lookup"><span data-stu-id="82d92-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d92-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82d92-141">Return value</span></span>

<span data-ttu-id="82d92-142">**NtReadFile** devuelve un estado \_ correcto o el código de error NTSTATUS adecuado.</span><span class="sxs-lookup"><span data-stu-id="82d92-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="82d92-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82d92-143">Remarks</span></span>

<span data-ttu-id="82d92-144">Los autores de llamadas de **NtReadFile** deben haber llamado ya a [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) con el archivo \_ Read \_ Data o Generic \_ Read Value establecido en el parámetro *DesiredAccess* .</span><span class="sxs-lookup"><span data-stu-id="82d92-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="82d92-145">Si la llamada anterior a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece el \_ indicador archivo \_ sin \_ almacenamiento en búfer intermedio en el parámetro *CreateOptions* en **NtCreateFile**, los parámetros *length* y *byteoffset (* de **NtReadFile** deben ser múltiplos del tamaño del sector.</span><span class="sxs-lookup"><span data-stu-id="82d92-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="82d92-146">Para obtener más información, vea **NtCreateFile**.</span><span class="sxs-lookup"><span data-stu-id="82d92-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="82d92-147">**NtReadFile** comienza a leer desde el *byteoffset (* determinado o la posición del archivo actual en el *búfer* especificado.</span><span class="sxs-lookup"><span data-stu-id="82d92-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="82d92-148">Finaliza la operación de lectura en una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="82d92-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="82d92-149">El búfer está lleno porque se ha leído el número de bytes especificado por el parámetro de *longitud* .</span><span class="sxs-lookup"><span data-stu-id="82d92-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="82d92-150">Por lo tanto, no se pueden colocar más datos en el búfer sin desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="82d92-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="82d92-151">Se alcanza el final del archivo durante la operación de lectura, por lo que no hay más datos en el archivo que se van a transferir al búfer.</span><span class="sxs-lookup"><span data-stu-id="82d92-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="82d92-152">Si el autor de la llamada abrió el archivo con la marca SYNCHRONIZE establecida en *DesiredAccess*, el subproceso que realiza la llamada puede sincronizarse con la finalización de la operación de lectura esperando en el identificador de archivo, *FileHandle*.</span><span class="sxs-lookup"><span data-stu-id="82d92-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="82d92-153">El identificador se señaliza cada vez que se completa una operación de e/s que se emitió en el identificador.</span><span class="sxs-lookup"><span data-stu-id="82d92-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="82d92-154">Sin embargo, el autor de la llamada no debe esperar en un identificador que se abrió para el acceso a archivos sincrónicos (la alerta de e/s sincrónica de archivo y de e/s sincrónica de archivo \_ \_ \_ \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="82d92-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="82d92-155">En este caso, **NtReadFile** espera en nombre del autor de la llamada y no devuelve ningún resultado hasta que se completa la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="82d92-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="82d92-156">El autor de la llamada puede esperar en el identificador de archivo sin ningún riesgo si se cumplen las tres condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="82d92-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="82d92-157">El identificador se abrió para el acceso asincrónico (es decir, \_ \_ \_  no se especificó ninguna marca de e/s sincrónica de archivo).</span><span class="sxs-lookup"><span data-stu-id="82d92-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="82d92-158">El identificador se usa solo para una operación de e/s a la vez.</span><span class="sxs-lookup"><span data-stu-id="82d92-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="82d92-159">**NtReadFile** devolvió el estado \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="82d92-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="82d92-160">Un controlador debe llamar a **NtReadFile** en el contexto del proceso del sistema si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="82d92-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="82d92-161">El controlador creó el identificador de archivo que pasa a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="82d92-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="82d92-162">**NtReadFile** notificará al controlador la finalización de e/s por medio de un evento creado por el controlador.</span><span class="sxs-lookup"><span data-stu-id="82d92-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="82d92-163">**NtReadFile** notificará al controlador de finalización de e/s por medio de una rutina de devolución de llamada APC que el controlador pasa a **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="82d92-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="82d92-164">Los identificadores de archivo y de evento solo son válidos en el contexto del proceso en el que se crean los identificadores.</span><span class="sxs-lookup"><span data-stu-id="82d92-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="82d92-165">Por lo tanto, para evitar brechas de seguridad, el controlador debe crear cualquier archivo o controlador de eventos que pase a **NtReadFile** en el contexto del proceso del sistema, en lugar del contexto del proceso en el que se encuentra el controlador.</span><span class="sxs-lookup"><span data-stu-id="82d92-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="82d92-166">Del mismo modo, se debe llamar a **NtReadFile** en el contexto del proceso del sistema si notifica al controlador de finalización de e/s por medio de una APC, ya que APC se activa siempre en el contexto del subproceso que emite la solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="82d92-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="82d92-167">Si el controlador llama a **NtReadFile** en el contexto de un proceso que no es el del sistema, el APC podría retrasarse indefinidamente, o podría no activarse en absoluto.</span><span class="sxs-lookup"><span data-stu-id="82d92-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="82d92-168">Para obtener más información sobre cómo trabajar con archivos, vea [usar archivos en un controlador](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="82d92-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="82d92-169">Los autores de llamadas de **NtReadFile** deben ejecutarse en IRQL = \_ nivel pasivo y con el [APC de kernel especial habilitado](/windows-hardware/drivers/kernel/disabling-apcs).</span><span class="sxs-lookup"><span data-stu-id="82d92-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="82d92-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d92-170">Requirements</span></span>



| <span data-ttu-id="82d92-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d92-171">Requirement</span></span> | <span data-ttu-id="82d92-172">Value</span><span class="sxs-lookup"><span data-stu-id="82d92-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d92-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d92-173">Minimum supported client</span></span><br/> | <span data-ttu-id="82d92-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82d92-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="82d92-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d92-175">Minimum supported server</span></span><br/> | <span data-ttu-id="82d92-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82d92-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="82d92-177">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="82d92-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="82d92-178"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="82d92-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="82d92-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82d92-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d92-180"><dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82d92-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="82d92-181">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82d92-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="82d92-182"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82d92-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="82d92-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82d92-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d92-184"><dt>Ntdll.dll (modo de usuario)</dt></span><span class="sxs-lookup"><span data-stu-id="82d92-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="82d92-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="82d92-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d92-186">**KeInitializeEvent**</span><span class="sxs-lookup"><span data-stu-id="82d92-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="82d92-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="82d92-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="82d92-188">**NtQueryInformationFile**</span><span class="sxs-lookup"><span data-stu-id="82d92-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="82d92-189">**NtSetInformationFile**</span><span class="sxs-lookup"><span data-stu-id="82d92-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="82d92-190">**NtWriteFile**</span><span class="sxs-lookup"><span data-stu-id="82d92-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
