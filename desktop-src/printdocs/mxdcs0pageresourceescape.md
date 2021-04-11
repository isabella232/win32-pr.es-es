---
description: La estructura de MXDC de los \_ recursos S0PAGE de la \_ estructura t \_ \_ es una \_ \_ estructura de encabezado de escape MXDC que se \_ concatena con una \_ estructura de recurso t de MXDC XPS \_ S0PAGE \_ \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: MXDC_S0PAGE_RESOURCE_ESCAPE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276776"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="e0d7c-103">\_ \_ \_ Estructura T de recurso MXDC S0PAGE \_</span><span class="sxs-lookup"><span data-stu-id="e0d7c-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="e0d7c-104">La estructura de MXDC de los **\_ \_ recursos S0PAGE \_ \_** de la estructura t es una estructura de [**encabezado de escape MXDC que se concatena \_ \_ \_**](mxdcescapeheader.md) con una estructura de [**\_ \_ \_ recurso \_ t de MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d7c-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0d7c-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="e0d7c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0d7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0d7c-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="e0d7c-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="e0d7c-108">Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en MXDCOP \_ set \_ S0PAGE \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="e0d7c-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="e0d7c-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="e0d7c-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="e0d7c-110">Una estructura [**MXDC \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) que representa un recurso, como un archivo de fuente o de imagen, en una página de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="e0d7c-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0d7c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0d7c-111">Remarks</span></span>

<span data-ttu-id="e0d7c-112">Esta estructura se pasa en el parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama a esa función con el escape de [**\_ escape MXDC**](mxdc-escape.md) , y el miembro **opCode** de la estructura MXDC de [**encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ set \_ S0PAGE \_ Resource**.</span><span class="sxs-lookup"><span data-stu-id="e0d7c-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="e0d7c-113">El resultado es un recurso de página que se envía a MXDC.</span><span class="sxs-lookup"><span data-stu-id="e0d7c-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="e0d7c-114">Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="e0d7c-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="e0d7c-115">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); sin embargo, puede haber más de una de estas llamadas entre las llamadas a **StartPage** y **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="e0d7c-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="e0d7c-116">El consumo de transmisión por secuencias es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el **código de operación** **MXDCOP \_ set \_ S0PAGE \_** para cada recurso de la página antes de llamar a **ExtEscape** con el **código de operación** MXDCOP **\_ set \_ S0PAGE**.  </span><span class="sxs-lookup"><span data-stu-id="e0d7c-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d7c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d7c-117">Requirements</span></span>



| <span data-ttu-id="e0d7c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d7c-118">Requirement</span></span> | <span data-ttu-id="e0d7c-119">Value</span><span class="sxs-lookup"><span data-stu-id="e0d7c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e0d7c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d7c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d7c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0d7c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d7c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d7c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e0d7c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0d7c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d7c-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d7c-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d7c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0d7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d7c-127">Impresión</span><span class="sxs-lookup"><span data-stu-id="e0d7c-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e0d7c-128">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="e0d7c-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="e0d7c-129">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0d7c-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e0d7c-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="e0d7c-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="e0d7c-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="e0d7c-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

