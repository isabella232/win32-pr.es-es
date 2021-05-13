---
description: Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El archivo seleccionado puede tener un nombre de archivo largo.
title: FM_GETFILESELLFN mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842396"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="6ee17-104">Mensaje \_ GETFILESELLFN de FM</span><span class="sxs-lookup"><span data-stu-id="6ee17-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="6ee17-105">Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="6ee17-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="6ee17-106">El archivo seleccionado puede tener un nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="6ee17-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ee17-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ee17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee17-108">*índice*</span><span class="sxs-lookup"><span data-stu-id="6ee17-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee17-109">Índice de base cero del archivo seleccionado que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="6ee17-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6ee17-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="6ee17-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee17-111">Dirección de una [**estructura \_ GETFILESEL de FMS**](fms-getfilesel.md) que recibe información sobre la selección.</span><span class="sxs-lookup"><span data-stu-id="6ee17-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee17-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ee17-112">Return value</span></span>

<span data-ttu-id="6ee17-113">Devuelve el índice de base cero del archivo seleccionado que se recuperó.</span><span class="sxs-lookup"><span data-stu-id="6ee17-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee17-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ee17-114">Remarks</span></span>

<span data-ttu-id="6ee17-115">Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones compatibles con la red) deben usar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="6ee17-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="6ee17-116">Una extensión puede usar el [**mensaje \_ FM GETSELCOUNTLFN**](fm-getselcountlfn.md) para recuperar el recuento de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="6ee17-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee17-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee17-117">Requirements</span></span>



| <span data-ttu-id="6ee17-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee17-118">Requirement</span></span> | <span data-ttu-id="6ee17-119">Value</span><span class="sxs-lookup"><span data-stu-id="6ee17-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee17-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee17-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ee17-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6ee17-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee17-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ee17-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ee17-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ee17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee17-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee17-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee17-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6ee17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee17-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="6ee17-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="6ee17-128">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="6ee17-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="6ee17-129">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="6ee17-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




