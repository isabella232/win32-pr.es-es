---
description: La \_ estructura de escape t de MXDC PrintTicket \_ \_ es una \_ estructura de encabezado de escape MXDC \_ \_ T concatenada con una \_ estructura MXDC PRINTTICKET \_ Data \_ t.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653029"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="b6a88-103">\_ \_ \_ Estructura T de MXDC PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="b6a88-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="b6a88-104">La estructura de **\_ \_ escape \_ t de MXDC PrintTicket** es una estructura de [**encabezado de \_ escape MXDC \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**MXDC \_ PRINTTICKET \_ Data \_ t**](mxdcprintticketpassthrough.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a88-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a88-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6a88-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="b6a88-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6a88-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6a88-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="b6a88-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="b6a88-108">Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en MXDCOP \_ PrintTicket Fixed \_ \_ Page, MXDCOP \_ PrintTicket \_ fixed \_ doc o MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.</span><span class="sxs-lookup"><span data-stu-id="b6a88-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="b6a88-109">**printTicketData**</span><span class="sxs-lookup"><span data-stu-id="b6a88-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="b6a88-110">Una estructura de [**\_ \_ datos \_ de PRINTTICKET MXDC**](mxdcprintticketpassthrough.md) que contiene la solicitud de impresión.</span><span class="sxs-lookup"><span data-stu-id="b6a88-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6a88-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a88-111">Remarks</span></span>

<span data-ttu-id="b6a88-112">Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama a esa función con el escape de [**\_ escape MXDC**](mxdc-escape.md) y el miembro **opCode** de la estructura MXDC de [**encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ \_ \_ Página fija de PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**.</span><span class="sxs-lookup"><span data-stu-id="b6a88-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="b6a88-113">El resultado es escribir la solicitud de impresión en el archivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b6a88-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="b6a88-114">Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="b6a88-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="b6a88-115">Si el **código de operación** se establece en la **\_ \_ \_ Página fija MXDCOP PRINTTICKET**, se debe realizar la llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="b6a88-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="b6a88-116">Si el **código de operación** se establece en **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la llamada a **ExtEscape** debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="b6a88-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a88-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a88-117">Requirements</span></span>



| <span data-ttu-id="b6a88-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a88-118">Requirement</span></span> | <span data-ttu-id="b6a88-119">Value</span><span class="sxs-lookup"><span data-stu-id="b6a88-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6a88-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a88-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6a88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6a88-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a88-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6a88-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6a88-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6a88-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6a88-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a88-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a88-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6a88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a88-127">Impresión</span><span class="sxs-lookup"><span data-stu-id="b6a88-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6a88-128">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b6a88-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="b6a88-129">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6a88-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b6a88-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="b6a88-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="b6a88-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="b6a88-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

