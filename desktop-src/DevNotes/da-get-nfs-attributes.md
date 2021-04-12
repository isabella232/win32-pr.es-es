---
description: El código de control de los atributos de das \_ Get \_ NFS \_ consulta información adicional sobre un recurso compartido de NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Código de control de DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538680"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="ee4fb-103">DA \_ obtiene \_ el \_ código de control de atributos NFS</span><span class="sxs-lookup"><span data-stu-id="ee4fb-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="ee4fb-104">El código de control de los **atributos de das \_ Get \_ NFS \_** consulta información adicional sobre un recurso compartido de NFS.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="ee4fb-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="ee4fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee4fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4fb-107">*hDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-108">Identificador de un archivo en el recurso compartido NFS.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="ee4fb-109">Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="ee4fb-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-110">*dwIoControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-111">The control code for the operation.</span></span> <span data-ttu-id="ee4fb-112">Use **\_ \_ \_ los atributos de das Get NFS** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="ee4fb-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4fb-114">No se utiliza con esta operación; se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-115">*nInBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-116">No se utiliza con esta operación; se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-117">*lpOutBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-118">Un puntero al búfer de salida, que contiene una estructura de **\_ \_ atributos de archivo NFS** .</span><span class="sxs-lookup"><span data-stu-id="ee4fb-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="ee4fb-119">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-120">*nOutBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-121">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-122">*lpBytesReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-123">Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="ee4fb-124">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="ee4fb-125">Si *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="ee4fb-126">Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="ee4fb-127">Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="ee4fb-128">Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="ee4fb-129">Si este parámetro no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="ee4fb-130">Para recuperar el número de bytes devueltos, llame a [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="ee4fb-131">Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-132">*lpOverlapped* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4fb-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-133">Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="ee4fb-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="ee4fb-134">Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="ee4fb-135">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="ee4fb-136">En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="ee4fb-137">De lo contrario, se produce un error imprevisible en la función.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="ee4fb-138">En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="ee4fb-139">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee4fb-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee4fb-140">Return value</span></span>

<span data-ttu-id="ee4fb-141">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="ee4fb-142">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="ee4fb-143">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4fb-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee4fb-144">Remarks</span></span>

<span data-ttu-id="ee4fb-145">Este código de control no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-145">This control code has no associated header file.</span></span> <span data-ttu-id="ee4fb-146">Debe definir el código de control y las estructuras de datos como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="ee4fb-147">Los miembros de la estructura se pueden describir de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fb-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-149">Un valor opaco que se usa para los tipos de archivo especiales, como archivos de bloque especial, especial de caracteres y FIFO.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-151">Un valor opaco que se usa para los tipos de archivo especiales, como archivos de bloque especial, especial de caracteres y FIFO.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**S**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-153">Un valor de 64 bits que representa los segundos desde el 1 de enero de 1970 (UTC).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-155">Número de nanosegundos que se van a agregar al miembro de **segundos** .</span><span class="sxs-lookup"><span data-stu-id="ee4fb-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-157">El tipo de archivo NFS del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="ee4fb-158">Tipo de archivo NFS</span><span class="sxs-lookup"><span data-stu-id="ee4fb-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="ee4fb-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee4fb-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ee4fb-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_registro de tipo NFS \_</span><span class="sxs-lookup"><span data-stu-id="ee4fb-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="ee4fb-161">Un archivo normal.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="ee4fb-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir de tipo NFS \_</span><span class="sxs-lookup"><span data-stu-id="ee4fb-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="ee4fb-163">Un directorio.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-163">A directory.</span></span><br/>              |
| <span data-ttu-id="ee4fb-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_tipo \_ BLK de NFS</span><span class="sxs-lookup"><span data-stu-id="ee4fb-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="ee4fb-165">Un archivo de bloque especial.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="ee4fb-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo de NFS \_ \_ Chr</span><span class="sxs-lookup"><span data-stu-id="ee4fb-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="ee4fb-167">Archivo especial de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="ee4fb-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo de NFS \_ \_ lnk</span><span class="sxs-lookup"><span data-stu-id="ee4fb-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="ee4fb-169">Vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="ee4fb-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo de NFS \_ \_ sock</span><span class="sxs-lookup"><span data-stu-id="ee4fb-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="ee4fb-171">Un socket de Windows.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="ee4fb-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo de NFS \_ \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="ee4fb-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="ee4fb-173">Un archivo FIFO.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="ee4fb-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-175">Modo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-177">Número de vínculos al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-179">El identificador de usuario (UID) de UNIX.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-181">El identificador de grupo (GID) de UNIX.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Ajusta**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-183">Tamaño del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Usa**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-185">Tamaño de archivo utilizado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-185">The file size used, in bytes.</span></span> <span data-ttu-id="ee4fb-186">Es el mismo que el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-188">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-190">Identificador del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**ID**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-192">Identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-194">Última hora de acceso.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-196">Hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-198">La hora del último cambio.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fb-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-200">Estructura **de \_ \_ atributos de archivo NFS** .</span><span class="sxs-lookup"><span data-stu-id="ee4fb-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="ee4fb-201">Para obtener descripciones más detalladas de los miembros de esta estructura, consulte la estructura **fattr3** en la especificación del protocolo NFS versión 3 (tal y como se define en [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="ee4fb-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="ee4fb-203">Especifica si la conexión en la que se creó el identificador del recurso compartido de NFS es a través del protocolo NFS versión 2 o NFS versión 3.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="ee4fb-204">Value</span><span class="sxs-lookup"><span data-stu-id="ee4fb-204">Value</span></span>                            | <span data-ttu-id="ee4fb-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee4fb-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="ee4fb-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="ee4fb-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="ee4fb-207">Versión 2 de NFS</span><span class="sxs-lookup"><span data-stu-id="ee4fb-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="ee4fb-208"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="ee4fb-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="ee4fb-209">NFS versión 3</span><span class="sxs-lookup"><span data-stu-id="ee4fb-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee4fb-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4fb-210">Requirements</span></span>



| <span data-ttu-id="ee4fb-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4fb-211">Requirement</span></span> | <span data-ttu-id="ee4fb-212">Value</span><span class="sxs-lookup"><span data-stu-id="ee4fb-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="ee4fb-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4fb-213">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4fb-214">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee4fb-214">None supported</span></span><br/>         |
| <span data-ttu-id="ee4fb-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4fb-215">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4fb-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee4fb-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="ee4fb-217">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ee4fb-217">End of client support</span></span><br/>    | <span data-ttu-id="ee4fb-218">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee4fb-218">None supported</span></span><br/>         |
| <span data-ttu-id="ee4fb-219">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ee4fb-219">End of server support</span></span><br/>    | <span data-ttu-id="ee4fb-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee4fb-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee4fb-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee4fb-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4fb-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
