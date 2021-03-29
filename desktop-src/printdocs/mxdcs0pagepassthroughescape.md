---
description: La \_ estructura MXDC S0PAGE \_ PASSTHROUGH \_ escape \_ t es una \_ estructura de encabezado de escape MXDC que se \_ \_ concatena con una estructura MXDC \_ S0PAGE \_ Data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360896"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="77018-103">MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ T Structure</span><span class="sxs-lookup"><span data-stu-id="77018-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="77018-104">La estructura **MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ t** es una estructura de [**\_ \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) que se concatena con una estructura [**MXDC \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .</span><span class="sxs-lookup"><span data-stu-id="77018-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="77018-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77018-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="77018-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="77018-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="77018-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="77018-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="77018-108">Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="77018-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="77018-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="77018-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="77018-110">Una estructura [**MxdcS0PageData**](mxdcs0pagedata.md) que representa una página de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="77018-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77018-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77018-111">Remarks</span></span>

<span data-ttu-id="77018-112">Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape [**de \_ escape MXDC**](mxdc-escape.md) y el miembro **opCode** de la estructura [**MXDC de encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="77018-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="77018-113">El resultado es que el convertidor de documentos XML de Microsoft (MXDC) pasa la página a la impresora sin procesarla.</span><span class="sxs-lookup"><span data-stu-id="77018-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="77018-114">Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="77018-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="77018-115">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="77018-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="77018-116">La aplicación que realiza la llamada es responsable de validar el XML de la página del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="77018-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="77018-117">El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="77018-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="77018-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77018-118">Requirements</span></span>



| <span data-ttu-id="77018-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77018-119">Requirement</span></span> | <span data-ttu-id="77018-120">Value</span><span class="sxs-lookup"><span data-stu-id="77018-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="77018-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77018-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77018-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="77018-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77018-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77018-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77018-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="77018-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77018-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77018-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77018-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="77018-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77018-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="77018-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77018-128">Impresión</span><span class="sxs-lookup"><span data-stu-id="77018-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="77018-129">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="77018-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="77018-130">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77018-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="77018-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="77018-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="77018-132">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="77018-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

