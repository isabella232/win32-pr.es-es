---
description: Crea un puerto de finalización de entrada/salida (e/s) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de e/s que todavía no está asociado a un identificador de archivo, lo que permite la asociación en otro momento.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: CreateIoCompletionPort (función) (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687655"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="3cfa9-103">CreateIoCompletionPort (función)</span><span class="sxs-lookup"><span data-stu-id="3cfa9-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="3cfa9-104">Crea un puerto de finalización de entrada/salida (e/s) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de e/s que todavía no está asociado a un identificador de archivo, lo que permite la asociación en otro momento.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="3cfa9-105">La Asociación de una instancia de un identificador de archivo abierto con un puerto de finalización de e/s permite que un proceso reciba una notificación de la realización de operaciones de e/s asincrónicas que impliquen ese identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="3cfa9-106">El término *identificador de archivo* tal como se usa aquí hace referencia a una abstracción del sistema que representa un punto de conexión de e/s superpuesto, no solo un archivo en disco.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="3cfa9-107">Los objetos del sistema que admiten e/s superpuestas como puntos de conexión de red, Sockets TCP, canalizaciones con nombre y ranuras de correo se pueden usar como identificadores de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="3cfa9-108">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3cfa9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cfa9-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="3cfa9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cfa9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cfa9-111">*FileHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa9-112">Identificador de archivo abierto o **\_ \_ valor de identificador no válido**.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="3cfa9-113">El identificador debe ser un objeto que admita e/s superpuesta.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="3cfa9-114">Si se proporciona un identificador, debe haberse abierto para la finalización de e/s superpuesta.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="3cfa9-115">Por ejemplo, debe especificar la marca de superposición de **\_ marcador \_ de archivo** al utilizar la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para obtener el identificador.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="3cfa9-116">Si se especifica un **\_ \_ valor de identificador no válido** , la función crea un puerto de finalización de e/s sin asociarlo a un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="3cfa9-117">En este caso, el parámetro *ExistingCompletionPort* debe ser **null** y se omitirá el parámetro *CompletionKey* .</span><span class="sxs-lookup"><span data-stu-id="3cfa9-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3cfa9-118">*ExistingCompletionPort* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa9-119">Identificador de un puerto de finalización de e/s existente o **null**.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="3cfa9-120">Si este parámetro especifica un puerto de finalización de e/s existente, la función lo asocia con el identificador especificado por el parámetro *FileHandle* .</span><span class="sxs-lookup"><span data-stu-id="3cfa9-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="3cfa9-121">La función devuelve el identificador del puerto de finalización de e/s existente si se realiza correctamente; no crea un nuevo puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="3cfa9-122">Si este parámetro es **null**, la función crea un nuevo puerto de finalización de e/s y, si el parámetro *FileHandle* es válido, lo asocia al nuevo puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="3cfa9-123">En caso contrario, no se produce ninguna asociación de identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="3cfa9-124">Si se realiza correctamente, la función devuelve el identificador al nuevo puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="3cfa9-125">*CompletionKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa9-126">La clave de finalización definida por el usuario por controlador que se incluye en cada paquete de finalización de e/s para el identificador de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="3cfa9-127">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3cfa9-128">*NumberOfConcurrentThreads* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa9-129">Número máximo de subprocesos que el sistema operativo puede permitir para procesar simultáneamente los paquetes de finalización de e/s para el puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="3cfa9-130">Se omite este parámetro si el parámetro *ExistingCompletionPort* no es **null**.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="3cfa9-131">Si este parámetro es cero, el sistema permite tantos subprocesos que se ejecutan simultáneamente como procesadores en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cfa9-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cfa9-132">Return value</span></span>

<span data-ttu-id="3cfa9-133">Si la función se ejecuta correctamente, el valor devuelto es el identificador de un puerto de finalización de e/s:</span><span class="sxs-lookup"><span data-stu-id="3cfa9-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="3cfa9-134">Si el parámetro *ExistingCompletionPort* era **null**, el valor devuelto es un nuevo identificador.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="3cfa9-135">Si el parámetro *ExistingCompletionPort* era un identificador de puerto de finalización de e/s válido, el valor devuelto es el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="3cfa9-136">Si el parámetro *FileHandle* era un identificador válido, ese identificador de archivo se asocia ahora con el puerto de finalización de e/s devuelto.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="3cfa9-137">Si se produce un error en la función, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="3cfa9-138">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="3cfa9-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cfa9-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cfa9-139">Remarks</span></span>

<span data-ttu-id="3cfa9-140">Se puede indicar al sistema de e/s que envíe paquetes de notificación de finalización de e/s a los puertos de finalización de e/s, donde se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="3cfa9-141">La función **CreateIoCompletionPort** proporciona esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="3cfa9-142">Un puerto de finalización de e/s y su identificador se asocian con el proceso que lo creó y no se pueden compartir entre los procesos.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="3cfa9-143">Sin embargo, un único identificador se compartirá entre los subprocesos del mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="3cfa9-144">**CreateIoCompletionPort** se puede usar en tres modos distintos:</span><span class="sxs-lookup"><span data-stu-id="3cfa9-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="3cfa9-145">Cree solo un puerto de finalización de e/s sin asociarlo a un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="3cfa9-146">Asociar un puerto de finalización de e/s existente con un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="3cfa9-147">Realice la creación y la asociación en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="3cfa9-148">Para crear un puerto de finalización de e/s sin asociarlo, establezca el parámetro *FileHandle* en el **valor de \_ identificador \_ no válido**, el parámetro *ExistingCompletionPort* en **null** y el parámetro *CompletionKey* en cero (que se omite en este caso).</span><span class="sxs-lookup"><span data-stu-id="3cfa9-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="3cfa9-149">Establezca el parámetro *NumberOfConcurrentThreads* en el valor de simultaneidad deseado para el nuevo puerto de finalización de e/s, o bien, cero para el valor predeterminado (el número de procesadores del sistema).</span><span class="sxs-lookup"><span data-stu-id="3cfa9-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="3cfa9-150">El identificador pasado en el parámetro *FileHandle* puede ser cualquier controlador que admita e/s superpuesta.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="3cfa9-151">Normalmente, se trata de un identificador abierto por la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mediante el uso de la marca de **\_ indicador \_ superpuesto de archivo** (por ejemplo, archivos, ranuras de correo y canalizaciones).</span><span class="sxs-lookup"><span data-stu-id="3cfa9-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="3cfa9-152">Los objetos creados por otras funciones como [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) también se pueden asociar a un puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="3cfa9-153">Para obtener un ejemplo de uso de sockets, consulte [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="3cfa9-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="3cfa9-154">Un identificador solo se puede asociar a un puerto de finalización de e/s y, una vez realizada la asociación, el identificador permanece asociado a ese puerto de finalización de e/s hasta que se cierra.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="3cfa9-155">Para obtener más información sobre la teoría del puerto de finalización de e/s, el uso y las funciones asociadas, consulte [puertos de finalización de e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="3cfa9-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="3cfa9-156">Se pueden asociar varios identificadores de archivo a un único puerto de finalización de e/s llamando a **CreateIoCompletionPort** varias veces con el mismo identificador de puerto de finalización de e/s en el parámetro *ExistingCompletionPort* y un identificador de archivo diferente en el parámetro *FileHandle* cada vez.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="3cfa9-157">Use el parámetro *CompletionKey* para ayudar a la aplicación a realizar un seguimiento de las operaciones de e/s que se han completado.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="3cfa9-158">**CreateIoCompletionPort** no usa este valor para el control funcional. en su lugar, se adjunta al identificador de archivo especificado en el parámetro *FileHandle* en el momento de la asociación con un puerto de finalización de e/s.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="3cfa9-159">Esta clave de finalización debe ser única para cada identificador de archivo y acompañará al identificador de archivo a lo largo del proceso de cola de finalización interna.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="3cfa9-160">Se devuelve en la llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) cuando llega un paquete de finalización.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="3cfa9-161">La función [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) también usa el parámetro *CompletionKey* para poner en cola sus propios paquetes de finalización especial.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="3cfa9-162">Una vez que una instancia de un identificador abierto está asociada a un puerto de finalización de e/s, no se puede usar en la función [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) porque estas funciones tienen sus propios mecanismos de e/s asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="3cfa9-163">Es mejor no compartir un identificador de archivo asociado a un puerto de finalización de e/s mediante el uso de la herencia de identificadores o una llamada a la función [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="3cfa9-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="3cfa9-164">Las operaciones realizadas con estos identificadores duplicados generan notificaciones de finalización.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="3cfa9-165">Se recomienda tener cuidado.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-165">Careful consideration is advised.</span></span>

<span data-ttu-id="3cfa9-166">El identificador de puerto de finalización de e/s y todos los identificadores de archivo asociados a ese puerto de terminación de e/s concreto se conocen como *referencias al puerto de terminación de e/s*.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="3cfa9-167">El puerto de finalización de e/s se libera cuando no hay más referencias a él.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="3cfa9-168">Por lo tanto, todos estos identificadores deben estar cerrados correctamente para liberar el puerto de finalización de e/s y sus recursos del sistema asociados.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="3cfa9-169">Una vez que se cumplen estas condiciones, cierre el identificador del puerto de finalización de e/s mediante una llamada a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="3cfa9-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="3cfa9-170">En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.</span><span class="sxs-lookup"><span data-stu-id="3cfa9-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="3cfa9-171">Technology</span><span class="sxs-lookup"><span data-stu-id="3cfa9-171">Technology</span></span>                                           | <span data-ttu-id="3cfa9-172">Compatible</span><span class="sxs-lookup"><span data-stu-id="3cfa9-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="3cfa9-173">Protocolo bloque de mensajes del servidor (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="3cfa9-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="3cfa9-174">Sí</span><span class="sxs-lookup"><span data-stu-id="3cfa9-174">Yes</span></span><br/> |
| <span data-ttu-id="3cfa9-175">Conmutación por error transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="3cfa9-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="3cfa9-176">Sí</span><span class="sxs-lookup"><span data-stu-id="3cfa9-176">Yes</span></span><br/> |
| <span data-ttu-id="3cfa9-177">SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)</span><span class="sxs-lookup"><span data-stu-id="3cfa9-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="3cfa9-178">Sí</span><span class="sxs-lookup"><span data-stu-id="3cfa9-178">Yes</span></span><br/> |
| <span data-ttu-id="3cfa9-179">Sistema de archivos Volumen compartido de clúster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="3cfa9-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="3cfa9-180">Sí</span><span class="sxs-lookup"><span data-stu-id="3cfa9-180">Yes</span></span><br/> |
| <span data-ttu-id="3cfa9-181">Sistema de archivos resistente a errores (ReFS)</span><span class="sxs-lookup"><span data-stu-id="3cfa9-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="3cfa9-182">Sí</span><span class="sxs-lookup"><span data-stu-id="3cfa9-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3cfa9-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cfa9-183">Requirements</span></span>



| <span data-ttu-id="3cfa9-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cfa9-184">Requirement</span></span> | <span data-ttu-id="3cfa9-185">Value</span><span class="sxs-lookup"><span data-stu-id="3cfa9-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfa9-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cfa9-186">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfa9-187">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3cfa9-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cfa9-188">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfa9-189">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="3cfa9-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3cfa9-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cfa9-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cfa9-191"><dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa9-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3cfa9-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3cfa9-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cfa9-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa9-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="3cfa9-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3cfa9-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cfa9-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa9-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="3cfa9-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cfa9-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="3cfa9-197">**Temas de información general**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="3cfa9-198">Funciones de administración de archivos</span><span class="sxs-lookup"><span data-stu-id="3cfa9-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="3cfa9-199">Puertos de finalización de e/s</span><span class="sxs-lookup"><span data-stu-id="3cfa9-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="3cfa9-200">Usar los encabezados de Windows</span><span class="sxs-lookup"><span data-stu-id="3cfa9-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="3cfa9-201">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="3cfa9-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="3cfa9-202">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="3cfa9-203">**AcceptEx**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="3cfa9-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="3cfa9-205">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="3cfa9-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="3cfa9-207">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="3cfa9-208">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="3cfa9-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="3cfa9-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="3cfa9-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

