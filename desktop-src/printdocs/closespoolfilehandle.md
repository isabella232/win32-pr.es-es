---
description: La función CloseSpoolFileHandle cierra un identificador a un archivo de cola de impresión asociado al trabajo de impresión actualmente enviado por la aplicación.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Función CloseSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677727"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="1232b-103">CloseSpoolFileHandle función)</span><span class="sxs-lookup"><span data-stu-id="1232b-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="1232b-104">La función **CloseSpoolFileHandle** cierra un identificador a un archivo de cola de impresión asociado al trabajo de impresión actualmente enviado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1232b-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="1232b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1232b-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="1232b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1232b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1232b-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1232b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1232b-108">Identificador de la impresora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="1232b-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="1232b-109">Debe ser el mismo identificador que se usó para obtener *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="1232b-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="1232b-110">*hSpoolFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1232b-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1232b-111">Identificador del archivo de cola que se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="1232b-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="1232b-112">Si no se ha llamado a [**CommitSpoolData**](commitspooldata.md) desde que se llamó a [**GetSpoolFileHandle**](getspoolfilehandle.md) , debe ser el mismo identificador que devolvió **GetSpoolFileHandle**.</span><span class="sxs-lookup"><span data-stu-id="1232b-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="1232b-113">De lo contrario, debe ser el identificador devuelto por la llamada más reciente a **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="1232b-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1232b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1232b-114">Return value</span></span>

<span data-ttu-id="1232b-115">**True**, si se realiza correctamente, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1232b-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1232b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1232b-116">Remarks</span></span>

<span data-ttu-id="1232b-117">La aplicación no debe llamar a [**ClosePrinter**](closeprinter.md) en *hPrinter* hasta que haya tenido acceso por última vez al archivo de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="1232b-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="1232b-118">Después, debe llamar a **CloseSpoolFileHandle** seguido de **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="1232b-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="1232b-119">Los intentos de obtener acceso al identificador de la cola de impresión una vez cerrado el *hPrinter* original producirán un error aunque no se haya cerrado el propio identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="1232b-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="1232b-120">**CloseSpoolFileHandle** producirá un error si se llama primero a **ClosePrinter** .</span><span class="sxs-lookup"><span data-stu-id="1232b-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="1232b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1232b-121">Requirements</span></span>



| <span data-ttu-id="1232b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1232b-122">Requirement</span></span> | <span data-ttu-id="1232b-123">Value</span><span class="sxs-lookup"><span data-stu-id="1232b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1232b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1232b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1232b-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1232b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1232b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1232b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1232b-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1232b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1232b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1232b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1232b-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1232b-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1232b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1232b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1232b-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1232b-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1232b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1232b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1232b-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1232b-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="1232b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1232b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1232b-135">Impresión</span><span class="sxs-lookup"><span data-stu-id="1232b-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1232b-136">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="1232b-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1232b-137">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="1232b-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="1232b-138">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="1232b-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




