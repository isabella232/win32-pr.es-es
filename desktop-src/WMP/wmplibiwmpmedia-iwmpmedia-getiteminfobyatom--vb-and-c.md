---
title: IWMPMedia getItemInfoByAtom, método
description: El método getItemInfoByAtom devuelve el valor del atributo con el número de índice especificado.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- método getItemInfoByAtom de Windows Media Player
- método getItemInfoByAtom Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671585"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="69f4b-106">IWMPMedia:: getItemInfoByAtom (método)</span><span class="sxs-lookup"><span data-stu-id="69f4b-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="69f4b-107">El método **getItemInfoByAtom** devuelve el valor del atributo con el número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="69f4b-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f4b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69f4b-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="69f4b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69f4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f4b-110">*lAtom* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69f4b-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f4b-111">**System. Int32** que especifica el índice en el que reside el atributo solicitado dentro del conjunto de atributos disponibles.</span><span class="sxs-lookup"><span data-stu-id="69f4b-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f4b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69f4b-112">Return value</span></span>

<span data-ttu-id="69f4b-113">**System. String** que es el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="69f4b-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f4b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69f4b-114">Remarks</span></span>

<span data-ttu-id="69f4b-115">Este método se puede utilizar para recuperar los metadatos de un elemento multimedia específico mediante un número de índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="69f4b-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="69f4b-116">La propiedad **attributeCount** se puede utilizar para determinar el número de atributos disponibles para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="69f4b-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="69f4b-117">También se puede usar el método **getMediaAtom** de la interfaz **IWMPMediaCollection** para recuperar el índice de un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="69f4b-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="69f4b-118">Esta técnica suele ser más eficaz que los métodos **getItemInfo** o **getItemInfoByType** al trabajar con listas de reproducción grandes.</span><span class="sxs-lookup"><span data-stu-id="69f4b-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="69f4b-119">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="69f4b-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="69f4b-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="69f4b-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69f4b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f4b-121">Requirements</span></span>



| <span data-ttu-id="69f4b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f4b-122">Requirement</span></span> | <span data-ttu-id="69f4b-123">Value</span><span class="sxs-lookup"><span data-stu-id="69f4b-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f4b-124">Versión</span><span class="sxs-lookup"><span data-stu-id="69f4b-124">Version</span></span><br/>   | <span data-ttu-id="69f4b-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="69f4b-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="69f4b-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69f4b-126">Namespace</span></span><br/> | <span data-ttu-id="69f4b-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69f4b-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69f4b-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="69f4b-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69f4b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="69f4b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f4b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="69f4b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f4b-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69f4b-132">**IWMPMedia. attributeCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69f4b-133">**IWMPMedia. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69f4b-134">**IWMPMedia. setItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69f4b-135">**IWMPMedia3. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69f4b-136">**IWMPMediaCollection. getMediaAtom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="69f4b-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





