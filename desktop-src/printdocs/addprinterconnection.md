---
description: La función AddPrinterConnection agrega una conexión a la impresora especificada para el usuario actual.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Función AddPrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911182"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="8145a-103">AddPrinterConnection función)</span><span class="sxs-lookup"><span data-stu-id="8145a-103">AddPrinterConnection function</span></span>

<span data-ttu-id="8145a-104">La función **AddPrinterConnection** agrega una conexión a la impresora especificada para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8145a-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8145a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8145a-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="8145a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8145a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8145a-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8145a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8145a-108">Puntero a una cadena terminada en null que especifica el nombre de una impresora a la que el usuario actual desea establecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="8145a-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8145a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8145a-109">Return value</span></span>

<span data-ttu-id="8145a-110">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8145a-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8145a-111">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8145a-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8145a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8145a-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8145a-113">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8145a-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8145a-114">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8145a-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8145a-115">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8145a-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8145a-116">Cuando Windows establece una conexión con una impresora, puede que tenga que copiar los archivos del controlador de impresora en el servidor al que está conectada la impresora.</span><span class="sxs-lookup"><span data-stu-id="8145a-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="8145a-117">Si el usuario no tiene permiso para copiar archivos en la ubicación adecuada, se produce un error en la función **AddPrinterConnection** y [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="8145a-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="8145a-118">Una conexión de impresora establecida mediante una llamada a **AddPrinterConnection** se enumerará cuando se llame a [**EnumPrinters**](enumprinters.md) con *dwType* establecido en \_ conexión de enumeración de impresora \_ .</span><span class="sxs-lookup"><span data-stu-id="8145a-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="8145a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8145a-119">Requirements</span></span>



| <span data-ttu-id="8145a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8145a-120">Requirement</span></span> | <span data-ttu-id="8145a-121">Value</span><span class="sxs-lookup"><span data-stu-id="8145a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8145a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8145a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8145a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8145a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8145a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8145a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8145a-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8145a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8145a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8145a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8145a-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8145a-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8145a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8145a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8145a-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8145a-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8145a-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8145a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8145a-131"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8145a-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8145a-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8145a-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8145a-133">**AddPrinterConnectionW** (Unicode) y **AddPrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8145a-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8145a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8145a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8145a-135">Impresión</span><span class="sxs-lookup"><span data-stu-id="8145a-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8145a-136">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8145a-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8145a-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="8145a-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="8145a-138">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="8145a-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="8145a-139">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="8145a-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

