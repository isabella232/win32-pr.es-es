---
description: La función StartDocPrinter notifica al administrador de trabajos de impresión que se va a poner en cola un documento para su impresión.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Función StartDocPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912642"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="b5028-103">StartDocPrinter función)</span><span class="sxs-lookup"><span data-stu-id="b5028-103">StartDocPrinter function</span></span>

<span data-ttu-id="b5028-104">La función **StartDocPrinter** notifica al administrador de trabajos de impresión que se va a poner en cola un documento para su impresión.</span><span class="sxs-lookup"><span data-stu-id="b5028-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5028-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5028-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b5028-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5028-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5028-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5028-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5028-108">Identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="b5028-108">A handle to the printer.</span></span> <span data-ttu-id="b5028-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="b5028-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b5028-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b5028-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5028-111">Versión de la estructura a la que apunta *pDocInfo* .</span><span class="sxs-lookup"><span data-stu-id="b5028-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="b5028-112">Este valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="b5028-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="b5028-113">*pDocInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5028-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5028-114">Puntero a una estructura [**de \_ información \_**](doc-info-1.md) de documento 1 que describe el documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="b5028-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5028-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5028-115">Return value</span></span>

<span data-ttu-id="b5028-116">Si la función se ejecuta correctamente, el valor devuelto identifica el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="b5028-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="b5028-117">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b5028-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5028-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5028-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5028-119">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b5028-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b5028-120">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5028-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b5028-121">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="b5028-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b5028-122">La secuencia típica para un trabajo de impresión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b5028-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="b5028-123">Para iniciar un trabajo de impresión, llame a **StartDocPrinter**.</span><span class="sxs-lookup"><span data-stu-id="b5028-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="b5028-124">Para comenzar cada página, llame a [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5028-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="b5028-125">Para escribir datos en una página, llame a [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5028-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="b5028-126">Para finalizar cada página, llame a [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5028-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="b5028-127">Repita 2, 3 y 4 para tantas páginas como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b5028-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="b5028-128">Para finalizar el trabajo de impresión, llame a [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5028-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="b5028-129">Tenga en cuenta que no es necesario llamar a [**StartPagePrinter**](startpageprinter.md) y [**EndPagePrinter**](endpageprinter.md) , por ejemplo, si el tipo de datos de impresión incluye la información de la página.</span><span class="sxs-lookup"><span data-stu-id="b5028-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="b5028-130">Cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="b5028-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="b5028-131">Por ejemplo, esto puede ocurrir cuando se imprimen archivos EMF de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="b5028-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="b5028-132">El límite de tamaño de página depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón del proceso.</span><span class="sxs-lookup"><span data-stu-id="b5028-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="b5028-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b5028-133">Examples</span></span>

<span data-ttu-id="b5028-134">Para obtener un programa de ejemplo que usa esta función, consulte [Cómo: imprimir con la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="b5028-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5028-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5028-135">Requirements</span></span>



| <span data-ttu-id="b5028-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5028-136">Requirement</span></span> | <span data-ttu-id="b5028-137">Value</span><span class="sxs-lookup"><span data-stu-id="b5028-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5028-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5028-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b5028-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5028-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b5028-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5028-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b5028-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5028-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b5028-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5028-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5028-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5028-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b5028-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5028-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5028-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5028-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b5028-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5028-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5028-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b5028-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b5028-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b5028-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5028-149">**StartDocPrinterW** (Unicode) y **StartDocPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5028-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="b5028-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5028-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5028-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="b5028-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="b5028-152">**Información de documento \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b5028-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="b5028-153">**Información de documento \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b5028-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="b5028-154">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="b5028-155">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b5028-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b5028-157">Impresión</span><span class="sxs-lookup"><span data-stu-id="b5028-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b5028-158">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b5028-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b5028-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b5028-160">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b5028-161">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="b5028-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




