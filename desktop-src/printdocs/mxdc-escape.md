---
description: La \_ función de escape de impresora MXDC escape permite a las aplicaciones escribir documentos en un archivo o en una impresora en formato XML Paper Specification (XPS) mediante el convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE función (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652681"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="6a1bd-103">MXDC \_ escape (función)</span><span class="sxs-lookup"><span data-stu-id="6a1bd-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="6a1bd-104">La función de escape de impresora **MXDC \_ escape** permite a las aplicaciones escribir documentos en un archivo o en una impresora en formato XML Paper Specification (XPS) mediante el convertidor de documentos XPS de Microsoft (MXDC).</span><span class="sxs-lookup"><span data-stu-id="6a1bd-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="6a1bd-105">Para realizar esta operación, llame a la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a1bd-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="6a1bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a1bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a1bd-108">*cámaras*</span><span class="sxs-lookup"><span data-stu-id="6a1bd-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1bd-109">Identificador del contexto del dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="6a1bd-110">*cbInput*</span><span class="sxs-lookup"><span data-stu-id="6a1bd-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1bd-111">Tamaño, en bytes, de los datos a los que apunta el parámetro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="6a1bd-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6a1bd-112">*lpszInData*</span><span class="sxs-lookup"><span data-stu-id="6a1bd-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1bd-113">Puntero a un búfer que contiene los datos de entrada, que siempre se almacenan en una de las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="6a1bd-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span><span class="sxs-lookup"><span data-stu-id="6a1bd-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="6a1bd-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span><span class="sxs-lookup"><span data-stu-id="6a1bd-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="6a1bd-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="6a1bd-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="6a1bd-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="6a1bd-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="6a1bd-118">Cada una de estas estructuras tiene un miembro OpCode que especifica lo que debe hacer el MXDC.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="6a1bd-119">Consulte MxdcEscapeHeader para obtener comentarios detallados sobre estos códigos.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="6a1bd-120">Código de operaciones (OpCode)</span><span class="sxs-lookup"><span data-stu-id="6a1bd-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="6a1bd-121">Acción</span><span class="sxs-lookup"><span data-stu-id="6a1bd-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="6a1bd-122"><dt>**MXDCOP \_ Get \_ nombreDeArchivo**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="6a1bd-123">Establece el parámetro *lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) en, o bien la ruta de acceso completa del archivo de salida como una cadena terminada en cero, o bien el tamaño de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="6a1bd-124"><dt>**MXDCOP \_ de \_ documento fijo de PRINTTICKET fijo \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="6a1bd-125">Asocia una incidencia de impresión a una secuencia de documento fijo XPS.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="6a1bd-126"><dt>**\_ \_ documento fijo de PRINTTICKET MXDCOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="6a1bd-127">Asocia una incidencia de impresión a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="6a1bd-128"><dt>**MXDCOP \_ \_ Página fija de PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="6a1bd-129">Asocia una incidencia de impresión a una página XPS.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="6a1bd-130"><dt>**MXDCOP \_ establecer \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="6a1bd-131">Envía el marcado XPS de la página actual a la salida.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="6a1bd-132"><dt>**\_Recurso MXDCOP set \_ S0PAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="6a1bd-133">Envía a la salida un recurso de la página, como una imagen o fuente.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="6a1bd-134"><dt>**MXDCOP \_ set \_ XPSPASSTHRU \_ Mode**</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="6a1bd-135">Coloca el MXDC en un estado de paso a través, lo que permite que una aplicación escriba XPS directamente en el archivo de salida sin ningún procesamiento por parte de MXDC.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="6a1bd-136">Se puede escribir un documento completo o incluso una secuencia de documento de esta manera.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6a1bd-137">*cbOutput*</span><span class="sxs-lookup"><span data-stu-id="6a1bd-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1bd-138">Tamaño, en bytes, de los datos a los que apunta el parámetro *lpszOutData* .</span><span class="sxs-lookup"><span data-stu-id="6a1bd-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6a1bd-139">*lpszOutData*</span><span class="sxs-lookup"><span data-stu-id="6a1bd-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1bd-140">Un puntero a un búfer que contiene los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a1bd-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a1bd-141">Return value</span></span>

<span data-ttu-id="6a1bd-142">Si la función se ejecuta correctamente, el valor devuelto es mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="6a1bd-143">Si se produce un error en la función o no se admite, el valor devuelto es menor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1bd-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a1bd-144">Remarks</span></span>

<span data-ttu-id="6a1bd-145">Este escape es compatible con MXDC y XPSDrv, pero no con GDI.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="6a1bd-146">Para determinar si el controlador de impresora es MXDC, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el escape [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6a1bd-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="6a1bd-147">Si el controlador es MXDC, **ExtEscape** devolverá la cadena terminada en cero, " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="6a1bd-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="6a1bd-148">Asegúrese de que el búfer al que hace referencia el parámetro *lpszOutData* es lo suficientemente grande como para contener esta cadena.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="6a1bd-149">Para determinar si el controlador de impresora es el controlador del escritor de documentos XPS de Microsoft Windows, confirme que el controlador de impresora es el MXDC y, a continuación, determine si el nombre del controlador de impresora es "escritor de documentos XPS de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="6a1bd-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="6a1bd-150">Para obtener el nombre del controlador de la impresora, utilice una de las técnicas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="6a1bd-151">Llame a [**GetPrinterDriver**](getprinterdriver.md) con el valor del parámetro *LEVEL* establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="6a1bd-152">El nombre del controlador de la impresora se devuelve en el miembro **pName** de la estructura de [**información del controlador \_ \_ 1**](driver-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1bd-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="6a1bd-153">or</span><span class="sxs-lookup"><span data-stu-id="6a1bd-153">or</span></span>  
<span data-ttu-id="6a1bd-154">Llame a [**GetPrinter**](getprinter.md) con el valor del parámetro *LEVEL* establecido en 2.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="6a1bd-155">El nombre del controlador de la impresora se devuelve en el miembro **pDriverName** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1bd-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="6a1bd-156">En la tabla siguiente se muestra dónde encontrar varios objetos en el archivo XPS en el que se escribirán varios tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="6a1bd-157">Object</span><span class="sxs-lookup"><span data-stu-id="6a1bd-157">Object</span></span>       | <span data-ttu-id="6a1bd-158">Ubicación en el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="6a1bd-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="6a1bd-159">Página fija</span><span class="sxs-lookup"><span data-stu-id="6a1bd-159">Fixed Page</span></span>   | <span data-ttu-id="6a1bd-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="6a1bd-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="6a1bd-161">Miniatura</span><span class="sxs-lookup"><span data-stu-id="6a1bd-161">Thumbnail</span></span>    | <span data-ttu-id="6a1bd-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="6a1bd-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="6a1bd-163">Imprimir vale</span><span class="sxs-lookup"><span data-stu-id="6a1bd-163">Print Ticket</span></span> | <span data-ttu-id="6a1bd-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="6a1bd-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="6a1bd-165">Fuente</span><span class="sxs-lookup"><span data-stu-id="6a1bd-165">Font</span></span>         | <span data-ttu-id="6a1bd-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="6a1bd-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="6a1bd-167">Imagen</span><span class="sxs-lookup"><span data-stu-id="6a1bd-167">Image</span></span>        | <span data-ttu-id="6a1bd-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="6a1bd-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="6a1bd-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a1bd-169">Requirements</span></span>



| <span data-ttu-id="6a1bd-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1bd-170">Requirement</span></span> | <span data-ttu-id="6a1bd-171">Value</span><span class="sxs-lookup"><span data-stu-id="6a1bd-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a1bd-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a1bd-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1bd-173">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a1bd-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a1bd-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a1bd-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1bd-175">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a1bd-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6a1bd-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a1bd-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a1bd-177"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a1bd-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a1bd-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a1bd-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1bd-179">Impresión</span><span class="sxs-lookup"><span data-stu-id="6a1bd-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="6a1bd-180">[Funciones de escape de impresora](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a1bd-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a1bd-181">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="6a1bd-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

