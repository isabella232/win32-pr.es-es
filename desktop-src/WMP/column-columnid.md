---
title: COLUMNA. columnID
description: El atributo columnID especifica o recupera un identificador de columna en el control de lista de reproducción.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUMNA. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699945"
---
# <a name="columncolumnid"></a><span data-ttu-id="29f78-104">COLUMNA. columnID</span><span class="sxs-lookup"><span data-stu-id="29f78-104">COLUMN.columnID</span></span>

<span data-ttu-id="29f78-105">El atributo **columnID** especifica o recupera un identificador de columna en el control de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="29f78-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="29f78-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="29f78-106">Possible Values</span></span>

<span data-ttu-id="29f78-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="29f78-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="29f78-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29f78-108">Remarks</span></span>

<span data-ttu-id="29f78-109">Los valores de **columnID** son los mismos que los que se usan con el método **getItemInfo** en un objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="29f78-110">Se puede obtener una lista mediante el uso de los *medios*. la propiedad **attributeCount** para determinar el número de atributos disponibles para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="29f78-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="29f78-111">Los números de índice se pueden usar con los *medios*. método **getAttributeName** para determinar los nombres de los atributos, que a su vez se pueden pasar a los *elementos multimedia*. **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="29f78-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="29f78-112">La propiedad **columnID** solo se puede establecer en estos valores, con la excepción de algunos valores que no pueden ser devueltos por los *medios*. **getAttributeName**.</span><span class="sxs-lookup"><span data-stu-id="29f78-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="29f78-113">Estos valores se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="29f78-113">These values are listed below.</span></span>



| <span data-ttu-id="29f78-114">Value</span><span class="sxs-lookup"><span data-stu-id="29f78-114">Value</span></span>     | <span data-ttu-id="29f78-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="29f78-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29f78-116">name</span><span class="sxs-lookup"><span data-stu-id="29f78-116">name</span></span>      | <span data-ttu-id="29f78-117">Muestra el nombre del objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="29f78-118">duration</span><span class="sxs-lookup"><span data-stu-id="29f78-118">duration</span></span>  | <span data-ttu-id="29f78-119">Muestra la duración del objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="29f78-120">sourceURL</span><span class="sxs-lookup"><span data-stu-id="29f78-120">sourceURL</span></span> | <span data-ttu-id="29f78-121">Muestra la dirección URL del objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="29f78-122">status</span><span class="sxs-lookup"><span data-stu-id="29f78-122">status</span></span>    | <span data-ttu-id="29f78-123">Muestra el estado de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="29f78-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="29f78-124">tamaño</span><span class="sxs-lookup"><span data-stu-id="29f78-124">size</span></span>      | <span data-ttu-id="29f78-125">Muestra el tamaño del archivo que representa el objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="29f78-126">extensión</span><span class="sxs-lookup"><span data-stu-id="29f78-126">extension</span></span> | <span data-ttu-id="29f78-127">Muestra la extensión de nombre de archivo del archivo que representa el objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="29f78-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="29f78-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29f78-128">Requirements</span></span>



| <span data-ttu-id="29f78-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f78-129">Requirement</span></span> | <span data-ttu-id="29f78-130">Value</span><span class="sxs-lookup"><span data-stu-id="29f78-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="29f78-131">Versión</span><span class="sxs-lookup"><span data-stu-id="29f78-131">Version</span></span><br/> | <span data-ttu-id="29f78-132">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="29f78-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29f78-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="29f78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f78-134">**COLUMN, elemento**</span><span class="sxs-lookup"><span data-stu-id="29f78-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="29f78-135">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="29f78-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="29f78-136">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="29f78-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="29f78-137">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="29f78-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="29f78-138">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="29f78-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





