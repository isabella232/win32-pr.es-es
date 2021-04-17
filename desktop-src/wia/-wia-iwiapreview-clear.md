---
description: 'Libera la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview. También libera el filtro de procesamiento de imágenes.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview:: CLEAR (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705691"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="edbed-104">IWiaPreview:: CLEAR (método)</span><span class="sxs-lookup"><span data-stu-id="edbed-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="edbed-105">Libera la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="edbed-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="edbed-106">También libera el filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="edbed-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edbed-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="edbed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbed-108">Parameters</span></span>

<span data-ttu-id="edbed-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="edbed-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edbed-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbed-110">Return value</span></span>

<span data-ttu-id="edbed-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="edbed-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbed-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edbed-112">Remarks</span></span>

<span data-ttu-id="edbed-113">En **IWiaPreview:: Desactive** el componente Windows Image Acquisition (WIA) 2,0 Preview libera todos los punteros de interfaz que almacena.</span><span class="sxs-lookup"><span data-stu-id="edbed-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="edbed-114">El componente de vista previa de WIA 2,0 mantiene las referencias a *pWiaItem2* y *pWiaTransferCallback* que se pasan a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="edbed-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="edbed-115">Para ser precisos, el componente de vista previa de WIA 2,0 mantiene una referencia a *pWiaItem2* y el filtro de procesamiento de imágenes del controlador, que a su vez mantiene una referencia a *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="edbed-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="edbed-116">En **IWiaPreview:: Clear**, el componente de vista previa de WIA 2,0 también libera su referencia a *pWiaItem2* y al filtro de procesamiento de imágenes, que a su vez libera su referencia a *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="edbed-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="edbed-117">El componente de vista previa de WIA 2,0 elimina la imagen almacenada en memoria caché y sin filtrar que almacena internamente.</span><span class="sxs-lookup"><span data-stu-id="edbed-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbed-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edbed-118">Requirements</span></span>



| <span data-ttu-id="edbed-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbed-119">Requirement</span></span> | <span data-ttu-id="edbed-120">Value</span><span class="sxs-lookup"><span data-stu-id="edbed-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edbed-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="edbed-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edbed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="edbed-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="edbed-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="edbed-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="edbed-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edbed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbed-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="edbed-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="edbed-127">IDL</span><span class="sxs-lookup"><span data-stu-id="edbed-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edbed-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="edbed-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




