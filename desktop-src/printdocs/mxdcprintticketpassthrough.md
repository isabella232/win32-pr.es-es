---
description: La \_ estructura MXDC PRINTTICKET \_ Data T contiene \_ un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión y la impresora, para pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909578"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="b977f-103">Estructura MXDC de \_ datos de PRINTTICKET \_ \_</span><span class="sxs-lookup"><span data-stu-id="b977f-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="b977f-104">La estructura **MXDC \_ PRINTTICKET \_ Data \_ T** contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión y la impresora, para pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b977f-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b977f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b977f-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="b977f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b977f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b977f-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="b977f-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="b977f-108">Tamaño de la solicitud de impresión en bytes.</span><span class="sxs-lookup"><span data-stu-id="b977f-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b977f-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="b977f-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="b977f-110">El vale de impresión del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b977f-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b977f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b977f-111">Remarks</span></span>

<span data-ttu-id="b977f-112">Esta estructura se anexa a una estructura [**de \_ \_ encabezado de \_ escape MXDC**](mxdcescapeheader.md) que tiene el miembro **opCode** establecido en **MXDCOP \_ PrintTicket \_ fixed \_ Page**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** para crear una estructura [**MXDC \_ PrintTicket de \_ escape \_ T**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="b977f-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="b977f-113">A continuación, se pasa la estructura **MXDC \_ PRINTTICKET de \_ escape \_ T** al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="b977f-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="b977f-114">El efecto es escribir la solicitud de impresión en el archivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b977f-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="b977f-115">Si el **código de operación** se establece en la **\_ \_ \_ Página fija MXDCOP PRINTTICKET**, se debe realizar la llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="b977f-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="b977f-116">Si el **código de operación** se establece en **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la llamada a **ExtEscape** debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="b977f-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="b977f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b977f-117">Requirements</span></span>



| <span data-ttu-id="b977f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b977f-118">Requirement</span></span> | <span data-ttu-id="b977f-119">Value</span><span class="sxs-lookup"><span data-stu-id="b977f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b977f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b977f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b977f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b977f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b977f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b977f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b977f-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b977f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b977f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b977f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b977f-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b977f-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b977f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b977f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b977f-127">Impresión</span><span class="sxs-lookup"><span data-stu-id="b977f-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b977f-128">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b977f-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="b977f-129">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b977f-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b977f-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="b977f-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="b977f-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="b977f-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

