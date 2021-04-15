---
description: En este tema se enumeran los métodos SaveAdd de la clase Image. Para obtener una lista completa de los métodos de la clase Image, consulte métodos de imagen.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Métodos Image. SaveAdd (Gdiplusheaders. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985318"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="ca0cd-104">Image. SaveAdd (métodos)</span><span class="sxs-lookup"><span data-stu-id="ca0cd-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="ca0cd-105">En este tema se enumeran los métodos SaveAdd de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ca0cd-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="ca0cd-106">Para obtener una lista completa de los métodos de la clase **Image** , consulte [métodos de imagen](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ca0cd-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="ca0cd-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ca0cd-107">Overload list</span></span>



| <span data-ttu-id="ca0cd-108">Método</span><span class="sxs-lookup"><span data-stu-id="ca0cd-108">Method</span></span>                                                                                               | <span data-ttu-id="ca0cd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca0cd-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0cd-110">[**SaveAdd (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca0cd-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="ca0cd-111">El método [**Image:: SaveAdd**](/previous-versions//ms535408(v=vs.85)) agrega un marco a un archivo o a una secuencia especificados en una llamada anterior al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="ca0cd-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="ca0cd-112">Utilice este método para guardar los marcos seleccionados de una imagen de varios marcos en otra imagen de varios marcos.</span><span class="sxs-lookup"><span data-stu-id="ca0cd-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="ca0cd-113">[**SaveAdd (imagen \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="ca0cd-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="ca0cd-114">El método [**Image:: SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) agrega un marco a un archivo o a una secuencia especificados en una llamada anterior al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="ca0cd-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="ca0cd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca0cd-115">Requirements</span></span>



| <span data-ttu-id="ca0cd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca0cd-116">Requirement</span></span> | <span data-ttu-id="ca0cd-117">Value</span><span class="sxs-lookup"><span data-stu-id="ca0cd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0cd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca0cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0cd-119">Solo aplicaciones de escritorio de Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="ca0cd-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ca0cd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca0cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0cd-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca0cd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ca0cd-122">Producto</span><span class="sxs-lookup"><span data-stu-id="ca0cd-122">Product</span></span><br/>                  | <span data-ttu-id="ca0cd-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="ca0cd-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="ca0cd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca0cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0cd-125"><dt>Gdiplusheaders. h (incluir gdiplus. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca0cd-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="ca0cd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca0cd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca0cd-127"><dt>Gdiplus. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca0cd-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
