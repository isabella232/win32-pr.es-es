---
description: La \_ estructura MXDC S0PAGE \_ Data \_ T contiene una página de documento XPS que se pasará al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815347"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="622b3-103">MXDC \_ S0PAGE \_ Data \_ T estructura</span><span class="sxs-lookup"><span data-stu-id="622b3-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="622b3-104">La estructura **MXDC \_ S0PAGE \_ Data \_ T** contiene una página de documento XPS que se pasará al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.</span><span class="sxs-lookup"><span data-stu-id="622b3-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="622b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="622b3-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="622b3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="622b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="622b3-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="622b3-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="622b3-108">Tamaño del búfer de salida, **bData**.</span><span class="sxs-lookup"><span data-stu-id="622b3-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="622b3-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="622b3-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="622b3-110">Página del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="622b3-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="622b3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="622b3-111">Remarks</span></span>

<span data-ttu-id="622b3-112">Esta estructura se anexa a una estructura [**\_ t de \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) (que tiene el código de **operación** establecido en MXDCOP \_ set \_ S0PAGE) para crear una estructura [**MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ T**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="622b3-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="622b3-113">A continuación, esa estructura se pasa al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con [**MXDC \_ escape**](mxdc-escape.md) como escape.</span><span class="sxs-lookup"><span data-stu-id="622b3-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="622b3-114">El resultado es que el MXDC pasa la página a la salida sin procesarla.</span><span class="sxs-lookup"><span data-stu-id="622b3-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="622b3-115">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="622b3-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="622b3-116">La aplicación que realiza la llamada es responsable de validar el XML de la página del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="622b3-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="622b3-117">El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="622b3-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="622b3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="622b3-118">Requirements</span></span>



| <span data-ttu-id="622b3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="622b3-119">Requirement</span></span> | <span data-ttu-id="622b3-120">Value</span><span class="sxs-lookup"><span data-stu-id="622b3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="622b3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="622b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="622b3-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="622b3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="622b3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="622b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="622b3-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="622b3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="622b3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="622b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="622b3-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="622b3-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="622b3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="622b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="622b3-128">Impresión</span><span class="sxs-lookup"><span data-stu-id="622b3-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="622b3-129">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="622b3-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="622b3-130">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="622b3-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="622b3-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="622b3-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="622b3-132">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="622b3-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

