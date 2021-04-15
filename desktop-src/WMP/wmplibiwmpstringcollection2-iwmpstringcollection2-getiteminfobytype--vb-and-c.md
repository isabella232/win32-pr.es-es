---
title: IWMPStringCollection2 getItemInfobyType, método
description: El método getItemInfoByType devuelve el valor correspondiente al índice, el nombre, el idioma y el índice del elemento de colección de cadenas especificado.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- método getItemInfobyType de Windows Media Player
- método getItemInfobyType Windows Media Player, interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Windows Media Player, método getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709114"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="dc90b-106">IWMPStringCollection2:: getItemInfobyType (método)</span><span class="sxs-lookup"><span data-stu-id="dc90b-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="dc90b-107">El método **getItemInfoByType** devuelve el valor correspondiente al índice, el nombre, el idioma y el índice del elemento de colección de cadenas especificado.</span><span class="sxs-lookup"><span data-stu-id="dc90b-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc90b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc90b-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="dc90b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc90b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc90b-110">*lCollectionIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc90b-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc90b-111">**System. Int32** que es el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="dc90b-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="dc90b-112">*bstrType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc90b-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc90b-113">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="dc90b-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="dc90b-114">*bstrLanguage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc90b-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc90b-115">**System. String** que indica el idioma.</span><span class="sxs-lookup"><span data-stu-id="dc90b-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="dc90b-116">Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="dc90b-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="dc90b-117">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="dc90b-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="dc90b-118">*lAttributeIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc90b-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc90b-119">**System. Int32** que es el índice de base cero del atributo.</span><span class="sxs-lookup"><span data-stu-id="dc90b-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc90b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc90b-120">Return value</span></span>

<span data-ttu-id="dc90b-121">**Objeto System. Object** que es el elemento de colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="dc90b-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc90b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc90b-122">Remarks</span></span>

<span data-ttu-id="dc90b-123">Este método admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="dc90b-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="dc90b-124">El método **getItemInfo** no admite atributos con varios valores o atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="dc90b-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="dc90b-125">Al pasar el valor "ChildList" en el parámetro *bstrType* , puede recuperar una nueva colección de cadenas que contiene los elementos secundarios de uno de los elementos de la colección de cadenas primaria.</span><span class="sxs-lookup"><span data-stu-id="dc90b-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="dc90b-126">Por ejemplo, si la colección primaria contiene una lista de AlbumIDs, puede usar este método para obtener una colección de cadenas secundarias que contenga todas las pistas de uno de los álbumes.</span><span class="sxs-lookup"><span data-stu-id="dc90b-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="dc90b-127">Este enfoque es más rápido y eficaz que llamar dos veces al método **IWMPMediaCollection2. getStringCollectionByQuery.** una vez para obtener una colección de AlbumIDs y una segunda vez para obtener una colección de pistas para un AlbumID determinado.</span><span class="sxs-lookup"><span data-stu-id="dc90b-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="dc90b-128">Para usar ChildList de la forma que se acaba de describir, la colección de cadenas primaria debe obtenerse de una colección de medios a través de **IWMPLibraryServices** y no mediante la propiedad **AxWindowsMediaPlayer. mediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="dc90b-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="dc90b-129">Al usar ChildList, pase el valor "ChildList" en el parámetro *bstrType* y el valor 0 en el parámetro *lAttributeIndex* .</span><span class="sxs-lookup"><span data-stu-id="dc90b-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="dc90b-130">Después, puede convertir el objeto que se devuelve a una interfaz **IWMPStringCollection2** para tener acceso a la lista secundaria.</span><span class="sxs-lookup"><span data-stu-id="dc90b-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="dc90b-131">Para usar este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dc90b-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="dc90b-132">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dc90b-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc90b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc90b-133">Requirements</span></span>



| <span data-ttu-id="dc90b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc90b-134">Requirement</span></span> | <span data-ttu-id="dc90b-135">Value</span><span class="sxs-lookup"><span data-stu-id="dc90b-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc90b-136">Versión</span><span class="sxs-lookup"><span data-stu-id="dc90b-136">Version</span></span><br/>   | <span data-ttu-id="dc90b-137">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="dc90b-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="dc90b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc90b-138">Namespace</span></span><br/> | <span data-ttu-id="dc90b-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc90b-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dc90b-140">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="dc90b-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc90b-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dc90b-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc90b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc90b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc90b-143">**Atributo AlbumID**</span><span class="sxs-lookup"><span data-stu-id="dc90b-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="dc90b-144">**Interfaz IWMPLibraryServices (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc90b-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc90b-145">**IWMPMediaCollection2. getStringCollectionByQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc90b-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc90b-146">**Interfaz IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="dc90b-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc90b-147">**IWMPStringCollection2. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dc90b-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





