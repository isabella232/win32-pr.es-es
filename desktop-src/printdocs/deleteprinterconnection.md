---
description: La función DeletePrinterConnection elimina una conexión a una impresora establecida por una llamada a AddPrinterConnection o ConnectToPrinterDlg.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: Función DeletePrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716799"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="660d9-103">DeletePrinterConnection función)</span><span class="sxs-lookup"><span data-stu-id="660d9-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="660d9-104">La función **DeletePrinterConnection** elimina una conexión a una impresora establecida por una llamada a [**AddPrinterConnection**](addprinterconnection.md) o [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span><span class="sxs-lookup"><span data-stu-id="660d9-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="660d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="660d9-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="660d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="660d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660d9-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="660d9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660d9-108">Puntero a una cadena terminada en null que especifica el nombre de la conexión de impresora que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="660d9-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660d9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="660d9-109">Return value</span></span>

<span data-ttu-id="660d9-110">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="660d9-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="660d9-111">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="660d9-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="660d9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="660d9-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="660d9-113">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="660d9-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="660d9-114">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="660d9-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="660d9-115">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="660d9-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="660d9-116">La función **DeletePrinterConnection** no elimina los archivos del controlador de impresora que se copiaron en el servidor al que está conectada la impresora.</span><span class="sxs-lookup"><span data-stu-id="660d9-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="660d9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660d9-117">Requirements</span></span>



| <span data-ttu-id="660d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="660d9-118">Requirement</span></span> | <span data-ttu-id="660d9-119">Value</span><span class="sxs-lookup"><span data-stu-id="660d9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660d9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="660d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="660d9-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="660d9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="660d9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="660d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="660d9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="660d9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="660d9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="660d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="660d9-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="660d9-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="660d9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="660d9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="660d9-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="660d9-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="660d9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="660d9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="660d9-129"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="660d9-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="660d9-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="660d9-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="660d9-131">**DeletePrinterConnectionW** (Unicode) y **DeletePrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="660d9-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="660d9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="660d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660d9-133">Impresión</span><span class="sxs-lookup"><span data-stu-id="660d9-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="660d9-134">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="660d9-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="660d9-135">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="660d9-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="660d9-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="660d9-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="660d9-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="660d9-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




