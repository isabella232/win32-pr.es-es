---
description: La interfaz IAMTimelineTrack proporciona métodos para manipular objetos de seguimiento en los servicios de edición de DirectShow (DES). Una pista contiene una lista de orígenes que se representan en la salida final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaz IAMTimelineTrack (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691028"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="b43cb-103">Interfaz IAMTimelineTrack</span><span class="sxs-lookup"><span data-stu-id="b43cb-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="b43cb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b43cb-104">\[Deprecated.</span></span> <span data-ttu-id="b43cb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b43cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b43cb-106">La `IAMTimelineTrack` interfaz proporciona métodos para manipular objetos de *seguimiento* en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="b43cb-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="b43cb-107">Una pista contiene una lista de orígenes que se representan en la salida final.</span><span class="sxs-lookup"><span data-stu-id="b43cb-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="b43cb-108">Es posible que los orígenes dentro de la misma pista no se superpongan.</span><span class="sxs-lookup"><span data-stu-id="b43cb-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="b43cb-109">Las pistas de vídeo pueden tener efectos y transiciones.</span><span class="sxs-lookup"><span data-stu-id="b43cb-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="b43cb-110">El motor de representación aplica efectos antes de aplicar las transiciones.</span><span class="sxs-lookup"><span data-stu-id="b43cb-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="b43cb-111">Las pistas de audio pueden tener efectos, pero no transiciones.</span><span class="sxs-lookup"><span data-stu-id="b43cb-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="b43cb-112">Para obtener más información, vea [el modelo Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="b43cb-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="b43cb-113">Para crear un objeto Track, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor de \_ tipo principal de la escala de tiempo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b43cb-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="b43cb-114">Puede consultar el puntero **IAMTimelineObj** devuelto para la `IAMTimelineTrack` interfaz.</span><span class="sxs-lookup"><span data-stu-id="b43cb-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="b43cb-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="b43cb-115">Members</span></span>

<span data-ttu-id="b43cb-116">La interfaz **IAMTimelineTrack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b43cb-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b43cb-117">**IAMTimelineTrack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b43cb-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="b43cb-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="b43cb-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b43cb-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="b43cb-119">Methods</span></span>

<span data-ttu-id="b43cb-120">La interfaz **IAMTimelineTrack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b43cb-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="b43cb-121">Método</span><span class="sxs-lookup"><span data-stu-id="b43cb-121">Method</span></span>                                                          | <span data-ttu-id="b43cb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b43cb-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b43cb-123">**AreYouBlank**</span><span class="sxs-lookup"><span data-stu-id="b43cb-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="b43cb-124">Determina si la pista está en blanco (no contiene objetos de origen).</span><span class="sxs-lookup"><span data-stu-id="b43cb-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="b43cb-125">**GetNextSrc**</span><span class="sxs-lookup"><span data-stu-id="b43cb-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="b43cb-126">Busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="b43cb-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="b43cb-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="b43cb-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="b43cb-128">Busca en la pista el siguiente origen que aparece en el momento especificado o posterior, con la especificada como valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b43cb-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="b43cb-129">**GetNextSrcEx**</span><span class="sxs-lookup"><span data-stu-id="b43cb-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="b43cb-130">Recupera el siguiente origen después del origen especificado.</span><span class="sxs-lookup"><span data-stu-id="b43cb-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="b43cb-131">**GetSourcesCount**</span><span class="sxs-lookup"><span data-stu-id="b43cb-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="b43cb-132">Recupera el número de orígenes de la pista.</span><span class="sxs-lookup"><span data-stu-id="b43cb-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="b43cb-133">**GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="b43cb-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="b43cb-134">Recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.</span><span class="sxs-lookup"><span data-stu-id="b43cb-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="b43cb-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="b43cb-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="b43cb-136">Recupera el objeto de origen más cercano al tiempo especificado, dado como un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b43cb-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="b43cb-137">**InsertSpace**</span><span class="sxs-lookup"><span data-stu-id="b43cb-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="b43cb-138">Divide los objetos que existen en el momento especificado e inserta espacio entre ellos.</span><span class="sxs-lookup"><span data-stu-id="b43cb-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="b43cb-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="b43cb-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="b43cb-140">Divide los objetos que existen en el momento especificado e inserta espacio entre ellos, utilizando los valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b43cb-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="b43cb-141">**MoveEverythingBy**</span><span class="sxs-lookup"><span data-stu-id="b43cb-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="b43cb-142">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b43cb-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="b43cb-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="b43cb-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="b43cb-144">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b43cb-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="b43cb-145">**SrcAdd**</span><span class="sxs-lookup"><span data-stu-id="b43cb-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="b43cb-146">Agrega un origen a la pista.</span><span class="sxs-lookup"><span data-stu-id="b43cb-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="b43cb-147">**ZeroBetween**</span><span class="sxs-lookup"><span data-stu-id="b43cb-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="b43cb-148">Quita todo de la pista entre las horas especificadas.</span><span class="sxs-lookup"><span data-stu-id="b43cb-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="b43cb-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="b43cb-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="b43cb-150">Quita todo de la pista entre las horas especificadas, dado como valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b43cb-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="b43cb-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b43cb-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b43cb-152">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b43cb-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b43cb-153">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b43cb-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b43cb-154">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b43cb-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b43cb-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43cb-155">Requirements</span></span>



| <span data-ttu-id="b43cb-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43cb-156">Requirement</span></span> | <span data-ttu-id="b43cb-157">Value</span><span class="sxs-lookup"><span data-stu-id="b43cb-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b43cb-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b43cb-158">Header</span></span><br/>  | <dl> <span data-ttu-id="b43cb-159"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43cb-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b43cb-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b43cb-160">Library</span></span><br/> | <dl> <span data-ttu-id="b43cb-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b43cb-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
