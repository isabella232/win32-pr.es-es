---
description: La clase CMediaType administra los tipos de medios. Esta clase hereda la estructura de \_ tipo de medio am \_ . Se puede convertir en una variable de tipo AM \_ media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Clase CMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670760"
---
# <a name="cmediatype-class"></a><span data-ttu-id="01c9d-105">Clase CMediaType</span><span class="sxs-lookup"><span data-stu-id="01c9d-105">CMediaType class</span></span>

![jerarquía de clases cmediatype](images/mtype01.png)

<span data-ttu-id="01c9d-107">La `CMediaType` clase administra los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="01c9d-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="01c9d-108">Esta clase hereda la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="01c9d-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="01c9d-109">Se puede convertir en una variable de tipo **AM \_ media \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="01c9d-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="01c9d-110">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="01c9d-110">Public Methods</span></span>                                                      | <span data-ttu-id="01c9d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c9d-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="01c9d-112">**CMediaType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="01c9d-113">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="01c9d-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="01c9d-114">**~ CMediaType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="01c9d-115">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="01c9d-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="01c9d-116">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="01c9d-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="01c9d-117">Establece el tipo de medio desde otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="01c9d-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="01c9d-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="01c9d-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="01c9d-119">Determina si se ha asignado un tipo principal a este objeto.</span><span class="sxs-lookup"><span data-stu-id="01c9d-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="01c9d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="01c9d-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="01c9d-121">Recupera el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="01c9d-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="01c9d-122">**SetType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="01c9d-123">Especifica el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="01c9d-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="01c9d-124">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="01c9d-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="01c9d-125">Recupera el subtipo.</span><span class="sxs-lookup"><span data-stu-id="01c9d-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="01c9d-126">**SetSubtype**</span><span class="sxs-lookup"><span data-stu-id="01c9d-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="01c9d-127">Especifica el subtipo.</span><span class="sxs-lookup"><span data-stu-id="01c9d-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="01c9d-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="01c9d-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="01c9d-129">Determina si los ejemplos tienen un tamaño fijo o un tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="01c9d-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="01c9d-130">**IsTemporalCompressed**</span><span class="sxs-lookup"><span data-stu-id="01c9d-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="01c9d-131">Determina si la secuencia utiliza la compresión temporal.</span><span class="sxs-lookup"><span data-stu-id="01c9d-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="01c9d-132">**GetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="01c9d-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="01c9d-133">Recupera el tamaño de la muestra.</span><span class="sxs-lookup"><span data-stu-id="01c9d-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="01c9d-134">**SetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="01c9d-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="01c9d-135">Especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="01c9d-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="01c9d-136">**SetVariableSize**</span><span class="sxs-lookup"><span data-stu-id="01c9d-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="01c9d-137">Especifica que los ejemplos no tienen un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="01c9d-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="01c9d-138">**SetTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="01c9d-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="01c9d-139">Especifica si los ejemplos se comprimen mediante la compresión temporal.</span><span class="sxs-lookup"><span data-stu-id="01c9d-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="01c9d-140">**Aplique**</span><span class="sxs-lookup"><span data-stu-id="01c9d-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="01c9d-141">Recupera un puntero al bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="01c9d-142">**FormatLength**</span><span class="sxs-lookup"><span data-stu-id="01c9d-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="01c9d-143">Recupera la longitud del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="01c9d-144">**SetFormatType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="01c9d-145">Especifica el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="01c9d-146">**FormatType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="01c9d-147">Recupera el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="01c9d-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="01c9d-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="01c9d-149">Especifica el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="01c9d-150">**ResetFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="01c9d-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="01c9d-151">Elimina el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="01c9d-152">**AllocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="01c9d-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="01c9d-153">Asigna memoria para el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="01c9d-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="01c9d-154">**ReallocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="01c9d-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="01c9d-155">Reasigna el bloque de formato a un nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="01c9d-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="01c9d-156">**InitMediaType**</span><span class="sxs-lookup"><span data-stu-id="01c9d-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="01c9d-157">Inicializa el tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="01c9d-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="01c9d-158">**MatchesPartial**</span><span class="sxs-lookup"><span data-stu-id="01c9d-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="01c9d-159">Determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="01c9d-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="01c9d-160">**IsPartiallySpecified**</span><span class="sxs-lookup"><span data-stu-id="01c9d-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="01c9d-161">Determina si el tipo de medio se define parcialmente.</span><span class="sxs-lookup"><span data-stu-id="01c9d-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="01c9d-162">Operadores</span><span class="sxs-lookup"><span data-stu-id="01c9d-162">Operators</span></span>                                                           | <span data-ttu-id="01c9d-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c9d-163">Description</span></span>                                                                    |
| [<span data-ttu-id="01c9d-164">**operador =**</span><span class="sxs-lookup"><span data-stu-id="01c9d-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="01c9d-165">Sobrecarga el operador de asignación para copiar un tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="01c9d-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="01c9d-166">**operador = =**</span><span class="sxs-lookup"><span data-stu-id="01c9d-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="01c9d-167">Comprueba la igualdad entre objetos `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="01c9d-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="01c9d-168">**operador! =**</span><span class="sxs-lookup"><span data-stu-id="01c9d-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="01c9d-169">Comprueba la desigualdad entre objetos `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="01c9d-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="01c9d-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01c9d-170">Requirements</span></span>



| <span data-ttu-id="01c9d-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c9d-171">Requirement</span></span> | <span data-ttu-id="01c9d-172">Value</span><span class="sxs-lookup"><span data-stu-id="01c9d-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c9d-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01c9d-173">Header</span></span><br/>  | <dl> <span data-ttu-id="01c9d-174"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01c9d-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="01c9d-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01c9d-175">Library</span></span><br/> | <dl> <span data-ttu-id="01c9d-176"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="01c9d-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




