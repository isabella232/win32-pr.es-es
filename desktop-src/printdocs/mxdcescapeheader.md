---
description: La \_ estructura del \_ encabezado de escape MXDC \_ contiene el código de operación para una llamada a ExtEscape con MXDC \_ escape como el parámetro nEscape. También proporciona los tamaños de los búferes de entrada y salida.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913146"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="8c212-104">MXDC \_ estructura de escape de \_ encabezado \_ T</span><span class="sxs-lookup"><span data-stu-id="8c212-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="8c212-105">La estructura del **\_ \_ encabezado \_ de escape MXDC** contiene el código de operación para una llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) como el parámetro *nEscape* .</span><span class="sxs-lookup"><span data-stu-id="8c212-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="8c212-106">También proporciona los tamaños de los búferes de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="8c212-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c212-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c212-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="8c212-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c212-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c212-109">**cbInput**</span><span class="sxs-lookup"><span data-stu-id="8c212-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="8c212-110">Tamaño del búfer de entrada que se pasará al parámetro *lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="8c212-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c212-111">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="8c212-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="8c212-112">Tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8c212-112">The size of the output buffer.</span></span> <span data-ttu-id="8c212-113">Este es el mismo valor que el parámetro *cbOutput* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="8c212-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c212-114">**Código**</span><span class="sxs-lookup"><span data-stu-id="8c212-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="8c212-115">Constante de código que indica a MXDC qué hacer.</span><span class="sxs-lookup"><span data-stu-id="8c212-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="8c212-116">Código de operaciones</span><span class="sxs-lookup"><span data-stu-id="8c212-116">Operations code</span></span>                      | <span data-ttu-id="8c212-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c212-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c212-118">MXDCOP \_ Get \_ nombreDeArchivo</span><span class="sxs-lookup"><span data-stu-id="8c212-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="8c212-119">Devuelve, en el parámetro *lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , la ruta de acceso completa del archivo de salida como una cadena terminada en cero o el tamaño de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="8c212-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="8c212-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8c212-120">See Remarks.</span></span>                   |
| <span data-ttu-id="8c212-121">MXDCOP \_ de \_ documento fijo de PRINTTICKET fijo \_ \_</span><span class="sxs-lookup"><span data-stu-id="8c212-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="8c212-122">Asocia una incidencia de impresión a una secuencia de documento fijo XPS.</span><span class="sxs-lookup"><span data-stu-id="8c212-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="8c212-123">\_ \_ documento fijo de PRINTTICKET MXDCOP \_</span><span class="sxs-lookup"><span data-stu-id="8c212-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="8c212-124">Asocia una incidencia de impresión a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="8c212-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="8c212-125">MXDCOP \_ \_ Página fija de PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="8c212-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="8c212-126">Asocia una incidencia de impresión a una página XPS.</span><span class="sxs-lookup"><span data-stu-id="8c212-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="8c212-127">MXDCOP \_ establecer \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="8c212-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="8c212-128">Envía el marcado XPS de la página actual a la salida.</span><span class="sxs-lookup"><span data-stu-id="8c212-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="8c212-129">\_Recurso MXDCOP set \_ S0PAGE \_</span><span class="sxs-lookup"><span data-stu-id="8c212-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="8c212-130">Envía a la salida un recurso de la página, como una imagen o fuente.</span><span class="sxs-lookup"><span data-stu-id="8c212-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="8c212-131">MXDCOP \_ set \_ XPSPASSTHRU \_ Mode</span><span class="sxs-lookup"><span data-stu-id="8c212-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="8c212-132">Coloca el MXDC en un estado de paso a través, lo que permite que una aplicación escriba XPS directamente en el archivo de salida sin ningún procesamiento por parte de MXDC.</span><span class="sxs-lookup"><span data-stu-id="8c212-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="8c212-133">Se puede escribir un documento completo o incluso una secuencia de documento de esta manera.</span><span class="sxs-lookup"><span data-stu-id="8c212-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c212-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c212-134">Remarks</span></span>

<span data-ttu-id="8c212-135">Antes de llamar a [**MXDC \_ escape**](mxdc-escape.md), \_ las aplicaciones deben comprobar primero que el controlador se MXDC llamando a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el escape [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8c212-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="8c212-136">Si el controlador es MXDC, la función devuelve la cadena terminada en cero " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="8c212-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="8c212-137">Esta estructura siempre está al principio de los datos pasados a la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) en su parámetro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="8c212-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="8c212-138">Cuando **opCode** es MXDCOP \_ Get \_ filename:</span><span class="sxs-lookup"><span data-stu-id="8c212-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="8c212-139">El parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) solo se compone de la estructura **\_ \_ \_ T del encabezado de escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="8c212-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="8c212-140">Para obtener el nombre de archivo de salida, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) dos veces.</span><span class="sxs-lookup"><span data-stu-id="8c212-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="8c212-141">La primera vez, pase 4 al parámetro *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="8c212-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="8c212-142">Establezca el parámetro *lpszOutData* para que apunte a cualquier 4 bytes de memoria asignados.</span><span class="sxs-lookup"><span data-stu-id="8c212-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="8c212-143">El tamaño de la ruta de acceso completa del archivo se devolverá en el parámetro *lpszOutData* de **ExtEscape**.</span><span class="sxs-lookup"><span data-stu-id="8c212-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="8c212-144">A continuación, llame de nuevo a la función.</span><span class="sxs-lookup"><span data-stu-id="8c212-144">Then call the function again.</span></span> <span data-ttu-id="8c212-145">Esta vez, establezca *cbOutput* y *cbInput* en 4 + *datasize*.</span><span class="sxs-lookup"><span data-stu-id="8c212-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="8c212-146">La ruta de acceso completa del archivo se devolverá en una estructura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .</span><span class="sxs-lookup"><span data-stu-id="8c212-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="8c212-147">Cuando **opCode** es MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq o MXDCOP \_ PrintTicket \_ fixed \_ doc:</span><span class="sxs-lookup"><span data-stu-id="8c212-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="8c212-148">El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="8c212-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="8c212-149">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="8c212-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="8c212-150">Cuando **opCode** es MXDCOP \_ \_ Página fija de PRINTTICKET \_ :</span><span class="sxs-lookup"><span data-stu-id="8c212-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="8c212-151">El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="8c212-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="8c212-152">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="8c212-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="8c212-153">Cuando **opCode** es MXDCOP \_ set \_ S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="8c212-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="8c212-154">El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenada en una estructura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="8c212-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="8c212-155">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="8c212-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="8c212-156">La aplicación que realiza la llamada es responsable de validar el XML.</span><span class="sxs-lookup"><span data-stu-id="8c212-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="8c212-157">El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ set \_ S0PAGE \_ Resource como **opCode** para cada recurso de la página antes de llamarlo con MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="8c212-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="8c212-158">Cuando **opCode** es MXDCOP \_ set \_ S0PAGE \_ Resource:</span><span class="sxs-lookup"><span data-stu-id="8c212-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="8c212-159">El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenada en una estructura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="8c212-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="8c212-160">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), pero puede haber varias llamadas de este tipo entre las llamadas a **StartPage** y **EndPage** .</span><span class="sxs-lookup"><span data-stu-id="8c212-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="8c212-161">El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ set \_ S0PAGE \_ Resource como **opCode** para cada recurso de la página antes de llamarlo con MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="8c212-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="8c212-162">Cuando **opCode** es MXDCOP \_ set \_ XPSPASSTHRU \_ Mode:</span><span class="sxs-lookup"><span data-stu-id="8c212-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="8c212-163">El parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) solo se compone de la estructura **\_ \_ \_ T del encabezado de escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="8c212-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="8c212-164">Esta llamada debe realizarse antes de la llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span><span class="sxs-lookup"><span data-stu-id="8c212-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c212-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c212-165">Requirements</span></span>



| <span data-ttu-id="8c212-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c212-166">Requirement</span></span> | <span data-ttu-id="8c212-167">Value</span><span class="sxs-lookup"><span data-stu-id="8c212-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8c212-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c212-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8c212-169">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c212-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c212-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c212-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8c212-171">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c212-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8c212-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c212-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c212-173"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c212-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c212-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c212-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c212-175">Impresión</span><span class="sxs-lookup"><span data-stu-id="8c212-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8c212-176">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8c212-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="8c212-177">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c212-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8c212-178">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="8c212-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="8c212-179">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="8c212-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

