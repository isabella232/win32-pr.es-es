---
title: IWMPMedia getItemInfo, método
description: El método getItemInfo devuelve el valor del atributo especificado para el elemento multimedia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671588"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="a76df-106">IWMPMedia:: getItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="a76df-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="a76df-107">El método **getItemInfo** devuelve el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="a76df-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a76df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a76df-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="a76df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a76df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a76df-110">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a76df-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a76df-111">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="a76df-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="a76df-112">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a76df-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a76df-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a76df-113">Return value</span></span>

<span data-ttu-id="a76df-114">**System. String** que es el valor del atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="a76df-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="a76df-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a76df-115">Remarks</span></span>

<span data-ttu-id="a76df-116">Este método devuelve los metadatos de un elemento multimedia individual o de un elemento multimedia que forma parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a76df-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="a76df-117">La propiedad **attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="a76df-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="a76df-118">Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible.</span><span class="sxs-lookup"><span data-stu-id="a76df-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="a76df-119">Los nombres de atributo individuales se pueden pasar a **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="a76df-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="a76df-120">Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="a76df-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="a76df-121">Si el elemento multimedia procede de una biblioteca que se ha recuperado mediante una llamada a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será distinto de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="a76df-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="a76df-122">Por ejemplo, los atributos disponibles en la biblioteca local recuperada mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles en la biblioteca local recuperada mediante **IWMPCore**.</span><span class="sxs-lookup"><span data-stu-id="a76df-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="a76df-123">Los demás orígenes definen el conjunto de atributos disponibles de otros orígenes (bibliotecas remotas, dispositivos portátiles o CDs).</span><span class="sxs-lookup"><span data-stu-id="a76df-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="a76df-124">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a76df-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a76df-125">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a76df-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a76df-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a76df-126">Requirements</span></span>



| <span data-ttu-id="a76df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a76df-127">Requirement</span></span> | <span data-ttu-id="a76df-128">Value</span><span class="sxs-lookup"><span data-stu-id="a76df-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76df-129">Versión</span><span class="sxs-lookup"><span data-stu-id="a76df-129">Version</span></span><br/>   | <span data-ttu-id="a76df-130">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a76df-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a76df-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a76df-131">Namespace</span></span><br/> | <span data-ttu-id="a76df-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a76df-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a76df-133">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a76df-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a76df-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a76df-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76df-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a76df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76df-136">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="a76df-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="a76df-137">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a76df-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a76df-138">**IWMPMedia. attributeCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a76df-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a76df-139">**IWMPMedia. getAttributeName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a76df-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a76df-140">**IWMPMedia. setItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a76df-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a76df-141">**IWMPMedia3. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a76df-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





