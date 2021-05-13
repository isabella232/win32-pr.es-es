---
description: Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).
title: FM_GETFILESEL mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841426"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="d719c-103">Mensaje \_ GETFILESEL de FM</span><span class="sxs-lookup"><span data-stu-id="d719c-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="d719c-104">Enviado por una extensión del Administrador de archivos para recuperar información sobre un archivo seleccionado desde la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="d719c-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="d719c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d719c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d719c-106">*índice*</span><span class="sxs-lookup"><span data-stu-id="d719c-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="d719c-107">Índice de base cero del archivo seleccionado que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="d719c-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d719c-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="d719c-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="d719c-109">Dirección de una [**estructura \_ GETFILESEL de FMS**](fms-getfilesel.md) que recibe información sobre la selección.</span><span class="sxs-lookup"><span data-stu-id="d719c-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d719c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d719c-110">Return value</span></span>

<span data-ttu-id="d719c-111">Devuelve el índice de base cero del archivo seleccionado que se recuperó.</span><span class="sxs-lookup"><span data-stu-id="d719c-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="d719c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d719c-112">Remarks</span></span>

<span data-ttu-id="d719c-113">Una extensión puede usar el [**mensaje \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar el recuento de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="d719c-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="d719c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d719c-114">Requirements</span></span>



| <span data-ttu-id="d719c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d719c-115">Requirement</span></span> | <span data-ttu-id="d719c-116">Value</span><span class="sxs-lookup"><span data-stu-id="d719c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d719c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d719c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d719c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d719c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d719c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d719c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d719c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d719c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d719c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d719c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d719c-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="d719c-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d719c-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d719c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d719c-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="d719c-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="d719c-125">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="d719c-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="d719c-126">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="d719c-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




