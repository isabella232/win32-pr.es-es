---
description: La función FlushPrinter envía un búfer a la impresora para borrarlo de un estado transitorio.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Función FlushPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545355"
---
# <a name="flushprinter-function"></a><span data-ttu-id="86edb-103">FlushPrinter función)</span><span class="sxs-lookup"><span data-stu-id="86edb-103">FlushPrinter function</span></span>

<span data-ttu-id="86edb-104">La función **FlushPrinter** envía un búfer a la impresora para borrarlo de un estado transitorio.</span><span class="sxs-lookup"><span data-stu-id="86edb-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="86edb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86edb-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="86edb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86edb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86edb-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86edb-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86edb-108">Identificador del objeto Printer.</span><span class="sxs-lookup"><span data-stu-id="86edb-108">A handle to the printer object.</span></span> <span data-ttu-id="86edb-109">Debe ser el mismo identificador que se utilizó en una llamada anterior a [**WritePrinter**](writeprinter.md) , por parte del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="86edb-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="86edb-110">*pBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86edb-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86edb-111">Puntero a una matriz de bytes que contiene los datos que se van a escribir en la impresora.</span><span class="sxs-lookup"><span data-stu-id="86edb-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="86edb-112">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86edb-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86edb-113">Tamaño, en bytes, de la matriz a la que apunta *pBuf*.</span><span class="sxs-lookup"><span data-stu-id="86edb-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="86edb-114">*pcWritten* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86edb-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86edb-115">Un puntero a un valor que recibe el número de bytes de datos que se escribieron en la impresora.</span><span class="sxs-lookup"><span data-stu-id="86edb-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="86edb-116">*cSleep* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86edb-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86edb-117">El tiempo, en milisegundos, durante el que la línea de e/s en el puerto de impresora debe mantenerse inactiva.</span><span class="sxs-lookup"><span data-stu-id="86edb-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86edb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86edb-118">Return value</span></span>

<span data-ttu-id="86edb-119">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="86edb-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="86edb-120">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="86edb-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="86edb-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86edb-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86edb-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="86edb-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="86edb-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="86edb-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="86edb-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="86edb-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="86edb-125">Solo se debe llamar a **FlushPrinter** si se produce un error de [**WritePrinter**](writeprinter.md) , lo que dejaría a la impresora en un estado transitorio.</span><span class="sxs-lookup"><span data-stu-id="86edb-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="86edb-126">Por ejemplo, la impresora puede entrar en un estado transitorio cuando se anula el trabajo y el controlador de impresora ha enviado parcialmente algunos datos sin procesar a la impresora.</span><span class="sxs-lookup"><span data-stu-id="86edb-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="86edb-127">**FlushPrinter** también puede especificar un período de inactividad durante el cual el administrador de trabajos de impresión no programa ningún trabajo en el puerto de impresora correspondiente.</span><span class="sxs-lookup"><span data-stu-id="86edb-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="86edb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86edb-128">Requirements</span></span>



| <span data-ttu-id="86edb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="86edb-129">Requirement</span></span> | <span data-ttu-id="86edb-130">Value</span><span class="sxs-lookup"><span data-stu-id="86edb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86edb-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86edb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="86edb-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86edb-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86edb-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86edb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="86edb-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86edb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86edb-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86edb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="86edb-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86edb-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="86edb-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86edb-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="86edb-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86edb-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="86edb-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86edb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86edb-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="86edb-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="86edb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="86edb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86edb-142">Impresión</span><span class="sxs-lookup"><span data-stu-id="86edb-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="86edb-143">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="86edb-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="86edb-144">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="86edb-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




