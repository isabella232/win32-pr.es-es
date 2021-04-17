---
description: La función ReadPrinter recupera datos de la impresora especificada.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Función ReadPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697331"
---
# <a name="readprinter-function"></a><span data-ttu-id="6ba3a-103">ReadPrinter función)</span><span class="sxs-lookup"><span data-stu-id="6ba3a-103">ReadPrinter function</span></span>

<span data-ttu-id="6ba3a-104">La función **ReadPrinter** recupera datos de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ba3a-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="6ba3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ba3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba3a-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ba3a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3a-108">Identificador del objeto Printer para el que se van a recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="6ba3a-109">Utilice la función [**OpenPrinter**](openprinter.md) para recuperar un identificador de objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="6ba3a-110">Use el formato: Nombreimpresora, trabajo xxxx.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3a-111">*pBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ba3a-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3a-112">Un puntero a un búfer que recibe los datos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3a-113">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ba3a-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3a-114">Tamaño, en bytes, del búfer al que apunta *pBuf* .</span><span class="sxs-lookup"><span data-stu-id="6ba3a-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3a-115">*pNoBytesRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ba3a-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba3a-116">Puntero a una variable que recibe el número de bytes de datos copiados en la matriz a la que apunta *pBuf* .</span><span class="sxs-lookup"><span data-stu-id="6ba3a-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba3a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba3a-117">Return value</span></span>

<span data-ttu-id="6ba3a-118">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6ba3a-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba3a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ba3a-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ba3a-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6ba3a-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6ba3a-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6ba3a-124">**ReadPrinter** devuelve un error si el dispositivo o la impresora no son bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="6ba3a-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba3a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba3a-125">Requirements</span></span>



| <span data-ttu-id="6ba3a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba3a-126">Requirement</span></span> | <span data-ttu-id="6ba3a-127">Value</span><span class="sxs-lookup"><span data-stu-id="6ba3a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba3a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ba3a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba3a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ba3a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ba3a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ba3a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba3a-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ba3a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ba3a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ba3a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba3a-133"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3a-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6ba3a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ba3a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ba3a-135"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3a-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6ba3a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ba3a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba3a-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3a-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6ba3a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba3a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba3a-139">Impresión</span><span class="sxs-lookup"><span data-stu-id="6ba3a-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6ba3a-140">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="6ba3a-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6ba3a-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6ba3a-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




