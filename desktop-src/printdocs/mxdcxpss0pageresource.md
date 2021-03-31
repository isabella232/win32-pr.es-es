---
description: La \_ estructura de recursos T de MXDC XPS \_ S0PAGE \_ \_ contiene información sobre un recurso, como una imagen o fuente, que está asociada a una página de documento XPS y que se va a pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910489"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="628f8-103">MXDC \_ XPS \_ S0PAGE \_ \_ estructura T</span><span class="sxs-lookup"><span data-stu-id="628f8-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="628f8-104">La estructura de **\_ \_ \_ recursos \_ T de MXDC XPS S0PAGE** contiene información sobre un recurso, como una imagen o fuente, que está asociada a una página de documento XPS y que se va a pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).</span><span class="sxs-lookup"><span data-stu-id="628f8-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="628f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="628f8-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="628f8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="628f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="628f8-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="628f8-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="628f8-108">Tamaño total de esta estructura y del recurso al que señala.</span><span class="sxs-lookup"><span data-stu-id="628f8-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="628f8-109">**dwResourceType**</span><span class="sxs-lookup"><span data-stu-id="628f8-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="628f8-110">Un valor de tipo [**\_ \_ \_ enumeración de página MXDC S0**](mxdcs0pageenums.md) que indica el tipo de recurso, como una imagen TIFF o una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="628f8-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="628f8-111">**szUri**</span><span class="sxs-lookup"><span data-stu-id="628f8-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="628f8-112">URI del recurso.</span><span class="sxs-lookup"><span data-stu-id="628f8-112">The URI of the resource.</span></span> <span data-ttu-id="628f8-113">No puede tener más de 260 bytes.</span><span class="sxs-lookup"><span data-stu-id="628f8-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="628f8-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="628f8-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="628f8-115">Tamaño del recurso en bytes.</span><span class="sxs-lookup"><span data-stu-id="628f8-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="628f8-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="628f8-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="628f8-117">Los datos del recurso en una matriz de bytes con el tamaño 1 + el tamaño del recurso.</span><span class="sxs-lookup"><span data-stu-id="628f8-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="628f8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="628f8-118">Remarks</span></span>

<span data-ttu-id="628f8-119">Esta estructura se anexa a una estructura [**\_ t de \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) (que tiene el **código de operación** establecido en **MXDCOP \_ set \_ S0PAGERESOURCE**) para crear una estructura de [**\_ \_ \_ escape \_ t de recurso MXDC S0PAGE**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="628f8-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="628f8-120">A continuación, se pasa la estructura de **\_ \_ \_ escape \_ T del recurso MXDC S0PAGE** resultante en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) a la que se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="628f8-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="628f8-121">El efecto es enviar el recurso a MXDC para la conversión y escribir en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="628f8-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="628f8-122">La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); sin embargo, puede haber más de una llamada de este tipo entre las llamadas a **StartPage** y **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="628f8-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="628f8-123">El consumo de transmisión por secuencias es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el **código de operación** **MXDCOP \_ set \_ S0PAGE \_** para cada recurso de la página antes de llamar a **ExtEscape** con el **código de operación** MXDCOP **\_ set \_ S0PAGE** .</span><span class="sxs-lookup"><span data-stu-id="628f8-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="628f8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="628f8-124">Requirements</span></span>



| <span data-ttu-id="628f8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="628f8-125">Requirement</span></span> | <span data-ttu-id="628f8-126">Value</span><span class="sxs-lookup"><span data-stu-id="628f8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="628f8-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="628f8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="628f8-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="628f8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="628f8-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="628f8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="628f8-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="628f8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="628f8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="628f8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="628f8-132"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="628f8-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="628f8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="628f8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628f8-134">Impresión</span><span class="sxs-lookup"><span data-stu-id="628f8-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="628f8-135">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="628f8-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="628f8-136">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="628f8-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="628f8-137">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="628f8-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="628f8-138">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="628f8-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

