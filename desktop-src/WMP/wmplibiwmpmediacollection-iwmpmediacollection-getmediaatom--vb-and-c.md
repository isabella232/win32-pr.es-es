---
title: IWMPMediaCollection getMediaAtom, método
description: El método getMediaAtom devuelve el índice de un atributo especificado en el conjunto de atributos disponibles.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- método getMediaAtom de Windows Media Player
- método getMediaAtom Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700337"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="35739-106">IWMPMediaCollection:: getMediaAtom (método)</span><span class="sxs-lookup"><span data-stu-id="35739-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="35739-107">El `getMediaAtom` método devuelve el índice de un atributo especificado en el conjunto de atributos disponibles.</span><span class="sxs-lookup"><span data-stu-id="35739-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="35739-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35739-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="35739-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35739-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35739-110">*bstrItemName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35739-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35739-111">**System. String** que es el nombre del elemento para el que se debe recuperar el índice.</span><span class="sxs-lookup"><span data-stu-id="35739-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35739-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35739-112">Return value</span></span>

<span data-ttu-id="35739-113">**System. Int32** que es el índice.</span><span class="sxs-lookup"><span data-stu-id="35739-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="35739-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35739-114">Remarks</span></span>

<span data-ttu-id="35739-115">El número de índice recuperado con este método se puede pasar a **IWMPMedia. getItemInfoByAtom** para tener acceso a los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="35739-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="35739-116">Esta técnica suele ser más eficaz al trabajar con listas de reproducción de gran tamaño que el acceso a un valor de atributo por nombre a través de **IWMPMedia. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="35739-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="35739-117">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="35739-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="35739-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="35739-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35739-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35739-119">Requirements</span></span>



| <span data-ttu-id="35739-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35739-120">Requirement</span></span> | <span data-ttu-id="35739-121">Value</span><span class="sxs-lookup"><span data-stu-id="35739-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35739-122">Versión</span><span class="sxs-lookup"><span data-stu-id="35739-122">Version</span></span><br/>   | <span data-ttu-id="35739-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="35739-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="35739-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35739-124">Namespace</span></span><br/> | <span data-ttu-id="35739-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="35739-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="35739-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="35739-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="35739-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="35739-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35739-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="35739-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35739-129">**IWMPMedia. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35739-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35739-130">**IWMPMedia. getItemInfoByAtom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35739-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35739-131">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35739-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





