---
title: Mensaje EM_DISPLAYBAND (RichEdit. h)
description: Muestra una parte del contenido de un control Rich Edit, como se formateó anteriormente para un dispositivo mediante el \_ mensaje em FORMATRANGE.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996651"
---
# <a name="em_displayband-message"></a><span data-ttu-id="c4629-104">\_Mensaje DISPLAYBAND em</span><span class="sxs-lookup"><span data-stu-id="c4629-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="c4629-105">Muestra una parte del contenido de un control Rich Edit, como se formateó anteriormente para un dispositivo mediante el mensaje [**em \_ FORMATRANGE**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="c4629-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4629-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4629-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4629-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4629-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c4629-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4629-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4629-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4629-110">Una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el área de presentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4629-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4629-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4629-111">Return value</span></span>

<span data-ttu-id="c4629-112">Si la operación se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="c4629-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="c4629-113">Si se produce un error en la operación, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="c4629-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4629-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4629-114">Remarks</span></span>

<span data-ttu-id="c4629-115">El rectángulo recorta el texto y los objetos del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="c4629-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="c4629-116">No es necesario que la aplicación establezca la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="c4629-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="c4629-117">El uso de bandas es el proceso por el que se genera una sola página de salida mediante uno o varios rectángulos o bandas independientes.</span><span class="sxs-lookup"><span data-stu-id="c4629-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="c4629-118">Cuando todas las bandas se colocan en la página, se obtiene una imagen completa.</span><span class="sxs-lookup"><span data-stu-id="c4629-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="c4629-119">Este enfoque suele usarse en impresoras de tramas que no tienen suficiente memoria o capacidad de imagen de una página completa al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c4629-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="c4629-120">Los dispositivos de bandas incluyen la mayoría de las impresoras matriciales, así como algunas impresoras láser.</span><span class="sxs-lookup"><span data-stu-id="c4629-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4629-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4629-121">Requirements</span></span>



| <span data-ttu-id="c4629-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4629-122">Requirement</span></span> | <span data-ttu-id="c4629-123">Value</span><span class="sxs-lookup"><span data-stu-id="c4629-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4629-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4629-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4629-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c4629-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4629-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4629-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4629-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4629-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4629-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4629-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4629-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4629-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4629-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4629-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4629-131">Imprimir controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c4629-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

