---
description: Obtiene una nueva secuencia para el elemento especificado.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback:: GetNextStream (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696519"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="0cb58-103">IWiaTransferCallback:: GetNextStream (método)</span><span class="sxs-lookup"><span data-stu-id="0cb58-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="0cb58-104">Obtiene una nueva secuencia para el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="0cb58-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cb58-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="0cb58-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cb58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb58-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb58-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="0cb58-108">Type: **LONG**</span></span>

<span data-ttu-id="0cb58-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="0cb58-109">Currently unused.</span></span> <span data-ttu-id="0cb58-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="0cb58-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0cb58-111">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb58-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0cb58-112">Type: **BSTR**</span></span>

<span data-ttu-id="0cb58-113">Especifica el nombre del elemento para el que se va a crear el flujo.</span><span class="sxs-lookup"><span data-stu-id="0cb58-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="0cb58-114">*bstrFullItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb58-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0cb58-115">Type: **BSTR**</span></span>

<span data-ttu-id="0cb58-116">Especifica el nombre completo del elemento para el que se va a crear el flujo.</span><span class="sxs-lookup"><span data-stu-id="0cb58-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="0cb58-117">*ppDestination* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb58-118">Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="0cb58-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="0cb58-119">Recibe la dirección de un puntero al nuevo objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="0cb58-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb58-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cb58-120">Return value</span></span>

<span data-ttu-id="0cb58-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0cb58-121">Type: **HRESULT**</span></span>

<span data-ttu-id="0cb58-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0cb58-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cb58-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cb58-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb58-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cb58-124">Remarks</span></span>

<span data-ttu-id="0cb58-125">Cuando este método se implementa mediante un filtro de procesamiento de imágenes, el minicontrolador de adquisición de imágenes de Windows (WIA) 2,0 lo llama durante la adquisición de la imagen para obtener la secuencia de destino del cliente.</span><span class="sxs-lookup"><span data-stu-id="0cb58-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="0cb58-126">**IWiaTransferCallback:: GetNextStream** de un filtro debe delegarse en el método de devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0cb58-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="0cb58-127">El filtro usa el flujo devuelto por la implementación de **IWiaTransferCallback:: GetNextStream** de la devolución de llamada de la aplicación para crear su propia secuencia que se devuelve al servicio WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0cb58-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="0cb58-128">El filtrado se realiza cuando el flujo del filtro llama al método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .</span><span class="sxs-lookup"><span data-stu-id="0cb58-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="0cb58-129">El flujo del filtro no puede realizar suposiciones sobre el número de bytes que se escriben en él en cada escritura, ya que los datos de la imagen sin filtrar pueden provienen del componente de vista previa de WIA 2,0 en lugar del controlador.</span><span class="sxs-lookup"><span data-stu-id="0cb58-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="0cb58-130">El componente de vista previa de WIA 2,0 escribe siempre los datos de imagen sin filtrar completos en el flujo del filtro solo una vez, lo que significa que el flujo del filtro tiene un origen que escribe en él.</span><span class="sxs-lookup"><span data-stu-id="0cb58-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="0cb58-131">Si el controlador y el componente de vista previa escriben en la secuencia del filtro, el flujo del filtro no puede suponer, por ejemplo, que recibirá el encabezado completo la primera vez que se llame a [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , aunque su controlador correspondiente siempre escribe primero los datos de encabezado en una sola escritura.</span><span class="sxs-lookup"><span data-stu-id="0cb58-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="0cb58-132">Tampoco puede suponer que una escritura posterior contenga exactamente una línea de exploración.</span><span class="sxs-lookup"><span data-stu-id="0cb58-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="0cb58-133">Por lo tanto, el flujo de filtrado puede tener que contar el número de bytes escritos en él para determinar, por ejemplo, dónde se inician los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0cb58-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="0cb58-134">La implementación **IWiaTransferCallback:: GetNextStream** del filtro de procesamiento de imágenes debe leer las propiedades necesarias para el procesamiento de imágenes del elemento para el que se adquiere la imagen.</span><span class="sxs-lookup"><span data-stu-id="0cb58-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="0cb58-135">El filtro no lee las propiedades directamente desde el *pWiaItem2* pasado a [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="0cb58-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="0cb58-136">En su lugar, el filtro debe llamar a [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) en este elemento de WIA 2,0 para obtener el elemento de WIA 2,0 real.</span><span class="sxs-lookup"><span data-stu-id="0cb58-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="0cb58-137">El motivo es que la imagen que se va a adquirir puede ser realmente un elemento secundario de *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="0cb58-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="0cb58-138">Por ejemplo, durante una adquisición de carpeta, el filtro usa *pWiaItem2* para obtener los elementos secundarios de *pWiaItem2* en **IWiaTransferCallback:: GetNextStream** (durante una adquisición de carpeta, el controlador devuelve las imágenes representadas por los elementos secundarios de *pWiaItem2*).</span><span class="sxs-lookup"><span data-stu-id="0cb58-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="0cb58-139">Lo mismo sucede cuando el componente WIA 2,0 Preview llama al filtro de procesamiento de imágenes que pasa un elemento secundario WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0cb58-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb58-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb58-140">Requirements</span></span>



| <span data-ttu-id="0cb58-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb58-141">Requirement</span></span> | <span data-ttu-id="0cb58-142">Value</span><span class="sxs-lookup"><span data-stu-id="0cb58-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb58-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb58-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb58-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0cb58-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb58-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb58-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb58-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0cb58-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cb58-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb58-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb58-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="0cb58-149">IDL</span><span class="sxs-lookup"><span data-stu-id="0cb58-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cb58-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cb58-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="0cb58-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cb58-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cb58-152"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cb58-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
