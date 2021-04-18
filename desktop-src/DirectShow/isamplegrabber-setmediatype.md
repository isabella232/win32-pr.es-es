---
description: El método SetMediaType especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber:: SetMediaType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681047"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="54e61-103">ISampleGrabber:: SetMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="54e61-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="54e61-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="54e61-104">\[Deprecated.</span></span> <span data-ttu-id="54e61-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54e61-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54e61-106">El `SetMediaType` método especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="54e61-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e61-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54e61-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="54e61-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54e61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e61-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="54e61-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="54e61-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica el tipo de medio requerido.</span><span class="sxs-lookup"><span data-stu-id="54e61-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="54e61-111">No es necesario establecer todos los miembros de la estructura; Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="54e61-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e61-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54e61-112">Return value</span></span>

<span data-ttu-id="54e61-113">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="54e61-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e61-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54e61-114">Remarks</span></span>

<span data-ttu-id="54e61-115">De forma predeterminada, el enganche de ejemplo no tiene ningún tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="54e61-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="54e61-116">Para asegurarse de que el enganche de ejemplo se conecta al filtro correcto, llame a este método antes de generar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="54e61-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="54e61-117">Este método restringe el intervalo de tipos de medios que el filtro aceptará.</span><span class="sxs-lookup"><span data-stu-id="54e61-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="54e61-118">Cuando el filtro se conecta, intenta coincidir con el tipo de medio proporcionado en *pType*.</span><span class="sxs-lookup"><span data-stu-id="54e61-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="54e61-119">Para ello, compara el tipo principal, el subtipo y los GUID de tipo de formato, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="54e61-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="54e61-120">Para cada uno de estos GUID, si *pType* tiene el valor \_ null GUID, el enganche de ejemplo acepta el tipo de medio sin ninguna comprobación adicional.</span><span class="sxs-lookup"><span data-stu-id="54e61-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="54e61-121">Si *pType* tiene cualquier otro valor, el enganche del ejemplo lo compara con el GUID del tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="54e61-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="54e61-122">A menos que los dos GUID coincidan exactamente, el enganche de ejemplo rechaza la conexión.</span><span class="sxs-lookup"><span data-stu-id="54e61-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="54e61-123">En el caso de los tipos de medios de vídeo, el enganche de ejemplo omite el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="54e61-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="54e61-124">Por lo tanto, aceptará cualquier tamaño de vídeo y velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="54e61-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="54e61-125">Cuando llame a `SetMediaType` , establezca el bloque de formato (**pbFormat**) en **null** y el tamaño (**cbFormat**) en cero.</span><span class="sxs-lookup"><span data-stu-id="54e61-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="54e61-126">En el caso de los tipos de medios de audio, el enganche de ejemplo examinará la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) y requerirá que el otro filtro se conecte con ese formato, a menos que el bloque de formato de *pType* sea **null**, o la etiqueta de formato sea PCM con formato de onda \_ \_ y los demás miembros de la estructura sean cero.</span><span class="sxs-lookup"><span data-stu-id="54e61-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="54e61-127">Ejemplo 1:</span><span class="sxs-lookup"><span data-stu-id="54e61-127">Example 1:</span></span>

-   <span data-ttu-id="54e61-128">Tipo principal: vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="54e61-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="54e61-129">Subtipo: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="54e61-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="54e61-130">Tipo de formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="54e61-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="54e61-131">El enganche de ejemplo aceptará cualquier tipo de vídeo en el que el tipo principal sea igual a MEDIATYPE \_ vídeo.</span><span class="sxs-lookup"><span data-stu-id="54e61-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="54e61-132">No comprobará el subtipo.</span><span class="sxs-lookup"><span data-stu-id="54e61-132">It will not check the subtype.</span></span>

<span data-ttu-id="54e61-133">Ejemplo 2:</span><span class="sxs-lookup"><span data-stu-id="54e61-133">Example 2:</span></span>

-   <span data-ttu-id="54e61-134">Tipo principal: vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="54e61-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="54e61-135">Subtipo: MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="54e61-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="54e61-136">Tipo de formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="54e61-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="54e61-137">Ahora, el enganche de ejemplo comprobará el subtipo y solo aceptará el vídeo RGB 24.</span><span class="sxs-lookup"><span data-stu-id="54e61-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="54e61-138">**Limitaciones:** Independientemente del tipo que establezca, el filtro de enganche de ejemplo rechaza los tipos de vídeo con orientación de arriba abajo ( *biheight* negativo) o con un tipo de formato de formato \_ VideoInfo2.</span><span class="sxs-lookup"><span data-stu-id="54e61-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="54e61-139">En este caso, aunque el `SetMediaType` método se ejecute correctamente, el filtro no se conectará.</span><span class="sxs-lookup"><span data-stu-id="54e61-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="54e61-140">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="54e61-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54e61-141">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54e61-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54e61-142">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="54e61-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54e61-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e61-143">Requirements</span></span>



| <span data-ttu-id="54e61-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e61-144">Requirement</span></span> | <span data-ttu-id="54e61-145">Value</span><span class="sxs-lookup"><span data-stu-id="54e61-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54e61-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54e61-146">Header</span></span><br/>  | <dl> <span data-ttu-id="54e61-147"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e61-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54e61-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54e61-148">Library</span></span><br/> | <dl> <span data-ttu-id="54e61-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54e61-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e61-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="54e61-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e61-151">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="54e61-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="54e61-152">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="54e61-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
