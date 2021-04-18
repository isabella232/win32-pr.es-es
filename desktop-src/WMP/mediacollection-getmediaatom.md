---
title: MediaCollection. getMediaAtom, método
description: El método getMediaAtom recupera el índice en el que un atributo especificado reside en el conjunto de atributos disponibles.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- método getMediaAtom de Windows Media Player
- método getMediaAtom de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690358"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="b7fbb-106">MediaCollection. getMediaAtom, método</span><span class="sxs-lookup"><span data-stu-id="b7fbb-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="b7fbb-107">El método **getMediaAtom** recupera el índice en el que un atributo especificado reside en el conjunto de atributos disponibles.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7fbb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7fbb-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="b7fbb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7fbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7fbb-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b7fbb-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7fbb-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-111">**String** containing the attribute name.</span></span> <span data-ttu-id="b7fbb-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7fbb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7fbb-113">Return value</span></span>

<span data-ttu-id="b7fbb-114">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="b7fbb-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7fbb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7fbb-115">Remarks</span></span>

<span data-ttu-id="b7fbb-116">El número de índice recuperado con este método se puede pasar a los *medios*. método **getItemInfoByAtom** para tener acceso a los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="b7fbb-117">Esta técnica suele ser más eficaz al trabajar con listas de reproducción de gran tamaño que el acceso a un valor de atributo por nombre a través de *medios*. **getItemInfo** o *multimedia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="b7fbb-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b7fbb-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b7fbb-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7fbb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7fbb-120">Requirements</span></span>



| <span data-ttu-id="b7fbb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7fbb-121">Requirement</span></span> | <span data-ttu-id="b7fbb-122">Value</span><span class="sxs-lookup"><span data-stu-id="b7fbb-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7fbb-123">Versión</span><span class="sxs-lookup"><span data-stu-id="b7fbb-123">Version</span></span><br/> | <span data-ttu-id="b7fbb-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b7fbb-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b7fbb-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7fbb-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b7fbb-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7fbb-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7fbb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7fbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7fbb-128">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b7fbb-129">**Media. getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="b7fbb-130">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="b7fbb-131">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b7fbb-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b7fbb-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b7fbb-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





