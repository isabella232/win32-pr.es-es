---
title: IWMPMedia3 getItemInfoByType, método
description: El método getItemInfoByType devuelve el valor del atributo correspondiente al tipo de atributo y el índice especificados.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, interfaz IWMPMedia3
- Interfaz IWMPMedia3 Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670363"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="cb3ee-106">IWMPMedia3:: getItemInfoByType (método)</span><span class="sxs-lookup"><span data-stu-id="cb3ee-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="cb3ee-107">El método **getItemInfoByType** devuelve el valor del atributo correspondiente al tipo de atributo y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3ee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb3ee-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="cb3ee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb3ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3ee-110">*bstrType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3ee-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3ee-111">**System. String** que es el tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="cb3ee-112">*bstrLanguage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3ee-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3ee-113">**System. String** que es el idioma.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-113">A **System.String** that is the language.</span></span> <span data-ttu-id="cb3ee-114">Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="cb3ee-115">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="cb3ee-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="cb3ee-116">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3ee-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3ee-117">**System. Int32** que es el índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3ee-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb3ee-118">Return value</span></span>

<span data-ttu-id="cb3ee-119">**Objeto System. Object** que es el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="cb3ee-120">El tipo al que se va a convertir este objeto depende del tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3ee-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb3ee-121">Remarks</span></span>

<span data-ttu-id="cb3ee-122">Este método devuelve los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="cb3ee-123">Este método admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="cb3ee-124">El método **getItemInfo** no admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="cb3ee-125">La propiedad **attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="cb3ee-126">Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="cb3ee-127">Los nombres de atributo individuales se pueden pasar al parámetro *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="cb3ee-128">El método **getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="cb3ee-129">Los números de índice se pueden pasar al parámetro de *Índice* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="cb3ee-130">Esto resulta útil cuando un elemento multimedia se ha clasificado en varios géneros, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="cb3ee-131">Si el elemento multimedia procede de una biblioteca que se ha recuperado mediante una llamada a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será distinto de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="cb3ee-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="cb3ee-132">Por ejemplo, los atributos disponibles en la biblioteca local recuperada mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles en la biblioteca local recuperada mediante **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="cb3ee-133">El conjunto de atributos disponibles de otros orígenes (bibliotecas remotas, dispositivos portátiles o CDs está definido por otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="cb3ee-134">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cb3ee-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="cb3ee-135">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cb3ee-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3ee-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb3ee-136">Requirements</span></span>



| <span data-ttu-id="cb3ee-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3ee-137">Requirement</span></span> | <span data-ttu-id="cb3ee-138">Value</span><span class="sxs-lookup"><span data-stu-id="cb3ee-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3ee-139">Versión</span><span class="sxs-lookup"><span data-stu-id="cb3ee-139">Version</span></span><br/>   | <span data-ttu-id="cb3ee-140">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="cb3ee-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cb3ee-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb3ee-141">Namespace</span></span><br/> | <span data-ttu-id="cb3ee-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb3ee-143">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="cb3ee-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb3ee-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb3ee-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3ee-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb3ee-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3ee-146">**Interfaz IWMPMedia3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb3ee-147">**IWMPMedia. attributeCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb3ee-148">**IWMPMedia. getAttributeName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb3ee-149">**IWMPMedia. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb3ee-150">**IWMPMedia3. getAttributeCountByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cb3ee-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





