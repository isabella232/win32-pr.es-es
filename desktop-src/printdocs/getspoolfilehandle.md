---
description: La función GetSpoolFileHandle recupera un identificador para el archivo de cola asociado al trabajo enviado actualmente por la aplicación.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Función GetSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083362"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="eeda4-103">GetSpoolFileHandle función)</span><span class="sxs-lookup"><span data-stu-id="eeda4-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="eeda4-104">La función **GetSpoolFileHandle** recupera un identificador para el archivo de cola asociado al trabajo enviado actualmente por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eeda4-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeda4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeda4-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="eeda4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeda4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeda4-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eeda4-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeda4-108">Identificador de la impresora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="eeda4-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="eeda4-109">Debe ser el mismo identificador que se usó para enviar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="eeda4-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="eeda4-110">(Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora).</span><span class="sxs-lookup"><span data-stu-id="eeda4-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeda4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeda4-111">Return value</span></span>

<span data-ttu-id="eeda4-112">Si la función se ejecuta correctamente, devuelve un identificador para el archivo de cola.</span><span class="sxs-lookup"><span data-stu-id="eeda4-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="eeda4-113">Si se produce un error en la función, devuelve un **\_ \_ valor de identificador no válido**.</span><span class="sxs-lookup"><span data-stu-id="eeda4-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeda4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeda4-114">Remarks</span></span>

<span data-ttu-id="eeda4-115">Con el identificador del archivo de cola de impresión, la aplicación puede escribir en el archivo de cola de impresión con llamadas a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguido de [**CommitSpoolData**](commitspooldata.md).</span><span class="sxs-lookup"><span data-stu-id="eeda4-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="eeda4-116">La aplicación no debe llamar a [**ClosePrinter**](closeprinter.md) en *hPrinter* hasta que haya tenido acceso por última vez al archivo de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="eeda4-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="eeda4-117">Después, debe llamar a [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguido de **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="eeda4-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="eeda4-118">Los intentos de obtener acceso al identificador de la cola de impresión una vez cerrado el *hPrinter* original producirán un error aunque no se haya cerrado el propio identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="eeda4-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="eeda4-119">**CloseSpoolFileHandle** producirá un error si se llama primero a **ClosePrinter** .</span><span class="sxs-lookup"><span data-stu-id="eeda4-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="eeda4-120">Esta función producirá un error si se llama antes de que el trabajo de impresión haya terminado de poner en cola.</span><span class="sxs-lookup"><span data-stu-id="eeda4-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeda4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeda4-121">Requirements</span></span>



| <span data-ttu-id="eeda4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeda4-122">Requirement</span></span> | <span data-ttu-id="eeda4-123">Value</span><span class="sxs-lookup"><span data-stu-id="eeda4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeda4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeda4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eeda4-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eeda4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eeda4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeda4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eeda4-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeda4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eeda4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeda4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeda4-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eeda4-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="eeda4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eeda4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eeda4-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeda4-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="eeda4-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeda4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeda4-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="eeda4-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="eeda4-134">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="eeda4-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eeda4-135">**GetSpoolFileHandleW** (Unicode) y **GetSpoolFileHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eeda4-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="eeda4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeda4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeda4-137">Impresión</span><span class="sxs-lookup"><span data-stu-id="eeda4-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eeda4-138">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="eeda4-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="eeda4-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="eeda4-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="eeda4-140">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="eeda4-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="eeda4-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="eeda4-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="eeda4-142">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="eeda4-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="eeda4-143">**CommitSpoolData**</span><span class="sxs-lookup"><span data-stu-id="eeda4-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

