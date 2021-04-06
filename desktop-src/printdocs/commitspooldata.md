---
description: La función CommitSpoolData notifica al administrador de trabajos de impresión que se ha escrito una cantidad de datos especificada en un archivo de cola especificado y está listo para ser representada.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Función CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909378"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="11f32-103">CommitSpoolData función)</span><span class="sxs-lookup"><span data-stu-id="11f32-103">CommitSpoolData function</span></span>

<span data-ttu-id="11f32-104">La función **CommitSpoolData** notifica al administrador de trabajos de impresión que se ha escrito una cantidad de datos especificada en un archivo de cola especificado y está listo para ser representada.</span><span class="sxs-lookup"><span data-stu-id="11f32-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11f32-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="11f32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f32-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11f32-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f32-108">Identificador de la impresora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="11f32-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="11f32-109">Debe ser el mismo identificador que se usó para obtener *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="11f32-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="11f32-110">*hSpoolFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11f32-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f32-111">Identificador del archivo de cola que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="11f32-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="11f32-112">En la primera llamada de **CommitSpoolData**, debe ser el mismo identificador devuelto por [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="11f32-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="11f32-113">Las llamadas subsiguientes a **CommitSpoolData** deben pasar el identificador devuelto por la llamada anterior.</span><span class="sxs-lookup"><span data-stu-id="11f32-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="11f32-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="11f32-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="11f32-115">*cbCommit*</span><span class="sxs-lookup"><span data-stu-id="11f32-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="11f32-116">Número de bytes confirmados en el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="11f32-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f32-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11f32-117">Return value</span></span>

<span data-ttu-id="11f32-118">Si la función se ejecuta correctamente, devuelve un identificador para el archivo de cola.</span><span class="sxs-lookup"><span data-stu-id="11f32-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="11f32-119">Si se produce un error en la función, devuelve un valor de identificador no válido \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="11f32-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="11f32-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11f32-120">Remarks</span></span>

<span data-ttu-id="11f32-121">Las aplicaciones que envían un trabajo de impresión del administrador de trabajos en cola pueden llamar a [**GetSpoolFileHandle**](getspoolfilehandle.md) y, a continuación, escribir los datos directamente en el identificador de la cola de impresión mediante una llamada a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span><span class="sxs-lookup"><span data-stu-id="11f32-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="11f32-122">Para notificar al administrador de trabajos de impresión que el archivo contiene datos que están listos para su representación, la aplicación debe llamar a **CommitSpoolData** y proporcionar el número de bytes disponibles.</span><span class="sxs-lookup"><span data-stu-id="11f32-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="11f32-123">Si se llama a **CommitSpoolData** varias veces, cada llamada debe usar el identificador de archivo de cola de impresión devuelto por la llamada anterior.</span><span class="sxs-lookup"><span data-stu-id="11f32-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="11f32-124">Cuando no se escriban más datos en el archivo de cola de impresión, se debe llamar a [**CloseSpoolFileHandle**](closespoolfilehandle.md) para el identificador de archivo devuelto por la última llamada a **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="11f32-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="11f32-125">Antes de llamar a **CommitSpoolData**, las aplicaciones deben establecer el puntero de archivo en la posición que tenía antes de escribir los datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="11f32-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="11f32-126">En el proceso de representar los datos en el archivo del administrador de trabajos de impresión, el administrador de trabajos de impresión moverá el puntero del archivo de cola de *cbCommit* bytes del valor actual del puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="11f32-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f32-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f32-127">Requirements</span></span>



| <span data-ttu-id="11f32-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f32-128">Requirement</span></span> | <span data-ttu-id="11f32-129">Value</span><span class="sxs-lookup"><span data-stu-id="11f32-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f32-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f32-130">Minimum supported client</span></span><br/> | <span data-ttu-id="11f32-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11f32-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="11f32-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f32-132">Minimum supported server</span></span><br/> | <span data-ttu-id="11f32-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11f32-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11f32-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11f32-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f32-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11f32-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="11f32-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11f32-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="11f32-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11f32-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="11f32-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11f32-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f32-139"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="11f32-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="11f32-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="11f32-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f32-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="11f32-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="11f32-142">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="11f32-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="11f32-143">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="11f32-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="11f32-144">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="11f32-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

