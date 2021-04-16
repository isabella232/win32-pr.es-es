---
description: La función WritePrinter notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Función WritePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716089"
---
# <a name="writeprinter-function"></a><span data-ttu-id="a28e8-103">WritePrinter función)</span><span class="sxs-lookup"><span data-stu-id="a28e8-103">WritePrinter function</span></span>

<span data-ttu-id="a28e8-104">La función **WritePrinter** notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="a28e8-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="a28e8-105">**WritePrinter** solo admite la impresión de GDI y no se debe utilizar para la impresión XPS.</span><span class="sxs-lookup"><span data-stu-id="a28e8-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="a28e8-106">Si el trabajo de impresión utiliza la ruta de impresión XPS o OpenXPS, use la [API de impresión XPS](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="a28e8-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="a28e8-107">No se admite el envío de trabajos de impresión XPS o OpenXPS al administrador de trabajos de impresión mediante **WritePrinter** y se pueden producir resultados indeterminados.</span><span class="sxs-lookup"><span data-stu-id="a28e8-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a28e8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a28e8-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="a28e8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a28e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28e8-110">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a28e8-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a28e8-111">Identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a28e8-111">A handle to the printer.</span></span> <span data-ttu-id="a28e8-112">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="a28e8-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a28e8-113">*pBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a28e8-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a28e8-114">Puntero a una matriz de bytes que contiene los datos que se deben escribir en la impresora.</span><span class="sxs-lookup"><span data-stu-id="a28e8-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="a28e8-115">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a28e8-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a28e8-116">Tamaño, en bytes, de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a28e8-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="a28e8-117">*pcWritten* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a28e8-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a28e8-118">Un puntero a un valor que recibe el número de bytes de datos que se escribieron en la impresora.</span><span class="sxs-lookup"><span data-stu-id="a28e8-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28e8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a28e8-119">Return value</span></span>

<span data-ttu-id="a28e8-120">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a28e8-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a28e8-121">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a28e8-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28e8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a28e8-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a28e8-123">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a28e8-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a28e8-124">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a28e8-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a28e8-125">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="a28e8-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a28e8-126">La secuencia de un trabajo de impresión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a28e8-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="a28e8-127">Para iniciar un trabajo de impresión, llame a [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="a28e8-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="a28e8-128">Para comenzar cada página, llame a [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="a28e8-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="a28e8-129">Para escribir datos en una página, llame a **WritePrinter**.</span><span class="sxs-lookup"><span data-stu-id="a28e8-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="a28e8-130">Para finalizar cada página, llame a [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="a28e8-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="a28e8-131">Repita 2, 3 y 4 para tantas páginas como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a28e8-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="a28e8-132">Para finalizar el trabajo de impresión, llame a [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="a28e8-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="a28e8-133">Cuando un documento de alto nivel (como un archivo de Adobe PDF o Microsoft Word) u otros datos de impresora (como PCL, PS o HPGL) se envían directamente a una impresora, la configuración de impresión definida en el documento tiene prioridad sobre la configuración de impresión de Windows.</span><span class="sxs-lookup"><span data-stu-id="a28e8-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="a28e8-134">La salida de los documentos cuando el valor del miembro *pDatatype* de la estructura [**doc \_ info \_ 1**](doc-info-1.md) que se pasó en el parámetro *PDOCINFO* de la llamada [**StartDocPrinter**](startdocprinter.md) es "RAW" debe describir completamente la configuración del trabajo de impresión de estilo [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)en el idioma comprendido por el hardware.</span><span class="sxs-lookup"><span data-stu-id="a28e8-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="a28e8-135">En versiones de Windows anteriores a Windows XP, cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="a28e8-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="a28e8-136">Por ejemplo, esto puede ocurrir cuando se imprimen archivos EMF de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="a28e8-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="a28e8-137">El límite de tamaño de página en las versiones de Windows anteriores a Windows XP depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón del proceso.</span><span class="sxs-lookup"><span data-stu-id="a28e8-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="a28e8-138">En Windows XP y versiones posteriores de Windows, los archivos EMF deben tener un tamaño de 2 GB o menos.</span><span class="sxs-lookup"><span data-stu-id="a28e8-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="a28e8-139">Si se usa **WritePrinter** para escribir datos que no sean EMF, como PDL listo para la impresión, el tamaño del archivo está limitado solo por el espacio disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="a28e8-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="a28e8-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a28e8-140">Examples</span></span>

<span data-ttu-id="a28e8-141">Para obtener un programa de ejemplo que usa esta función, consulte [Cómo: imprimir con la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="a28e8-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a28e8-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a28e8-142">Requirements</span></span>



| <span data-ttu-id="a28e8-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a28e8-143">Requirement</span></span> | <span data-ttu-id="a28e8-144">Value</span><span class="sxs-lookup"><span data-stu-id="a28e8-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a28e8-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a28e8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a28e8-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a28e8-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a28e8-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a28e8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a28e8-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a28e8-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a28e8-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a28e8-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28e8-150"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a28e8-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a28e8-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a28e8-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="a28e8-152"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a28e8-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a28e8-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a28e8-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a28e8-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a28e8-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a28e8-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="a28e8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28e8-156">Impresión</span><span class="sxs-lookup"><span data-stu-id="a28e8-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a28e8-157">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a28e8-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a28e8-158">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="a28e8-159">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a28e8-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a28e8-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="a28e8-162">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a28e8-163">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="a28e8-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

