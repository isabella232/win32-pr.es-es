---
description: Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Función AddPrinterConnection2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677731"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="bcad4-103">AddPrinterConnection2 función)</span><span class="sxs-lookup"><span data-stu-id="bcad4-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="bcad4-104">Agrega una conexión a la impresora especificada para el usuario actual y especifica los detalles de conexión.</span><span class="sxs-lookup"><span data-stu-id="bcad4-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcad4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcad4-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bcad4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcad4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcad4-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcad4-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcad4-108">Identificador de la ventana primaria en la que se mostrará el cuadro de diálogo si el sistema de impresión debe descargar un controlador de impresora del servidor de impresión para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="bcad4-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="bcad4-109">*pszName empiezan* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcad4-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcad4-110">Puntero a una cadena terminada en null que especifica el nombre de la impresora a la que el usuario actual desea conectarse.</span><span class="sxs-lookup"><span data-stu-id="bcad4-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="bcad4-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="bcad4-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="bcad4-112">Versión de la estructura a la que apunta *pConnectionInfo*.</span><span class="sxs-lookup"><span data-stu-id="bcad4-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="bcad4-113">Actualmente, solo se define el nivel 1, por lo que el valor de *dwLevel* debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="bcad4-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="bcad4-114">*pConnectionInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcad4-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcad4-115">Un puntero a una estructura de la [**\_ \_ información \_ de conexión**](printer-connection-info-1.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bcad4-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="bcad4-116">Vea la sección Comentarios para obtener más información sobre este parámetro.</span><span class="sxs-lookup"><span data-stu-id="bcad4-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcad4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcad4-117">Return value</span></span>

<span data-ttu-id="bcad4-118">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bcad4-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bcad4-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="bcad4-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="bcad4-120">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="bcad4-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="bcad4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcad4-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bcad4-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bcad4-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bcad4-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bcad4-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bcad4-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="bcad4-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bcad4-125">Cuando Windows Vista establece una conexión con una impresora, puede que sea necesario copiar los archivos del controlador de impresora del servidor al que está conectada la impresora.</span><span class="sxs-lookup"><span data-stu-id="bcad4-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="bcad4-126">Si el usuario no tiene permiso para copiar archivos en la ubicación adecuada, se produce un error en la función **AddPrinterConnection2** y [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="bcad4-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="bcad4-127">Si los archivos del controlador de impresora se deben copiar desde el servidor de impresión, pero no se pueden copiar silenciosamente debido a las directivas de grupo que están en vigor y la conexión de la impresora \_ \_ no \_ se establece la interfaz de usuario en *pConnectionInfo->dwFlags*, no se mostrará ningún cuadro de diálogo y se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="bcad4-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="bcad4-128">Si el controlador de impresora local se puede usar para representar trabajos de impresión para esta impresora y la versión del controlador local no debe coincidir con la versión del controlador de impresora en el servidor, establezca la coincidencia de conexión de impresora \_ \_ en *PConnectionInfo->dwFlags* y asigne el puntero a una variable de cadena que contenga la ruta de acceso al controlador de impresora local a *pConnectionInfo->pszDriverName*.</span><span class="sxs-lookup"><span data-stu-id="bcad4-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="bcad4-129">Una conexión de impresora que se establece mediante una llamada a **AddPrinterConnection2** se enumerará cuando se llame a [**EnumPrinters**](enumprinters.md) con *dwType* establecido en \_ conexión de enumeración de impresora \_ .</span><span class="sxs-lookup"><span data-stu-id="bcad4-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="bcad4-130">La versión ANSI de esta función, **AddPrinterConnection2A**, no se admite y devuelve un **error \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="bcad4-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcad4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcad4-131">Requirements</span></span>



| <span data-ttu-id="bcad4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcad4-132">Requirement</span></span> | <span data-ttu-id="bcad4-133">Value</span><span class="sxs-lookup"><span data-stu-id="bcad4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcad4-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcad4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bcad4-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bcad4-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bcad4-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcad4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bcad4-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcad4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bcad4-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcad4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcad4-139"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcad4-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bcad4-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcad4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="bcad4-141"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcad4-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bcad4-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bcad4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcad4-143"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bcad4-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bcad4-144">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bcad4-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bcad4-145">**AddPrinterConnection2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="bcad4-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="bcad4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcad4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcad4-147">Impresión</span><span class="sxs-lookup"><span data-stu-id="bcad4-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bcad4-148">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="bcad4-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bcad4-149">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="bcad4-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="bcad4-150">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="bcad4-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="bcad4-151">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="bcad4-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

