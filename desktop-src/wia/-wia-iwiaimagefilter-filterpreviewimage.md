---
description: Filtra la imagen de vista previa.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter:: FilterPreviewImage (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715344"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="8ea53-103">IWiaImageFilter:: FilterPreviewImage (método)</span><span class="sxs-lookup"><span data-stu-id="8ea53-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="8ea53-104">Filtra la imagen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="8ea53-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ea53-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="8ea53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ea53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea53-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea53-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8ea53-108">Type: **LONG**</span></span>

<span data-ttu-id="8ea53-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8ea53-109">Not used.</span></span> <span data-ttu-id="8ea53-110">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="8ea53-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8ea53-111">*pWiaChildItem2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea53-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8ea53-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="8ea53-113">Elemento que se procesa.</span><span class="sxs-lookup"><span data-stu-id="8ea53-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="8ea53-114">_InputImageExtents \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea53-115">Tipo: **Rect**</span><span class="sxs-lookup"><span data-stu-id="8ea53-115">Type: **RECT**</span></span>

<span data-ttu-id="8ea53-116">Las coordenadas (en el área de adquisición física) de la imagen que el componente de vista previa almacena internamente en caché.</span><span class="sxs-lookup"><span data-stu-id="8ea53-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="8ea53-117">*pInputStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea53-118">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="8ea53-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="8ea53-119">Puntero a la interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) para los datos de la imagen almacenada en caché que se filtran.</span><span class="sxs-lookup"><span data-stu-id="8ea53-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea53-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ea53-120">Return value</span></span>

<span data-ttu-id="8ea53-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8ea53-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8ea53-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8ea53-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ea53-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ea53-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea53-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ea53-124">Remarks</span></span>

<span data-ttu-id="8ea53-125">No llame a este método directamente desde su aplicación.</span><span class="sxs-lookup"><span data-stu-id="8ea53-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="8ea53-126">*pWiaChildItem2* debe ser un elemento secundario del *pWiaItem2* que se pasó a [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="8ea53-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="8ea53-127">*InputImageExtents* es necesario porque el filtro de procesamiento de imágenes es responsable de recortar el área de imagen que *pWiaChildItem2* representa de los datos de imagen pasados a través de *pInputStream*.</span><span class="sxs-lookup"><span data-stu-id="8ea53-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="8ea53-128">Una aplicación debe asegurarse de que *pWiaChildItem2* tiene el mismo formato de imagen \_ ( \_ formato de IPA de WIA), resolución (IP \_ de WIA \_ XRES y WIA \_ IPS \_ YRES) y profundidad de bits ( \_ \_ profundidad de IPA de WIA) que tenía *pWiaItem2* cuando se pasó a [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="8ea53-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea53-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea53-129">Requirements</span></span>



| <span data-ttu-id="8ea53-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea53-130">Requirement</span></span> | <span data-ttu-id="8ea53-131">Value</span><span class="sxs-lookup"><span data-stu-id="8ea53-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea53-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ea53-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea53-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ea53-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ea53-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea53-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ea53-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ea53-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ea53-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea53-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea53-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ea53-138">IDL</span><span class="sxs-lookup"><span data-stu-id="8ea53-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ea53-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ea53-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
