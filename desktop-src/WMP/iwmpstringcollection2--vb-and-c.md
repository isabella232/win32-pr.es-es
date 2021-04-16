---
title: Interfaz IWMPStringCollection2 (VB y C) (WMP. h)
description: Proporciona métodos que complementan la interfaz IWMPStringCollection.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB y C) interfaz de Windows Media Player
- IWMPStringCollection2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699796"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="b8321-105">Interfaz IWMPStringCollection2 (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="b8321-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="b8321-106">Proporciona métodos que complementan la interfaz **IWMPStringCollection** .</span><span class="sxs-lookup"><span data-stu-id="b8321-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b8321-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8321-107">Members</span></span>

<span data-ttu-id="b8321-108">La interfaz **IWMPStringCollection2 (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8321-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="b8321-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8321-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b8321-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8321-110">Methods</span></span>

<span data-ttu-id="b8321-111">La interfaz **IWMPStringCollection2 (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b8321-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="b8321-112">Método</span><span class="sxs-lookup"><span data-stu-id="b8321-112">Method</span></span>                                                                                                                 | <span data-ttu-id="b8321-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8321-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8321-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="b8321-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="b8321-115">Devuelve el número de atributos asociados con el índice del elemento de colección de cadenas, el nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="b8321-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="b8321-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b8321-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="b8321-117">Devuelve la cadena correspondiente al índice y el nombre del elemento de colección de cadenas especificado.</span><span class="sxs-lookup"><span data-stu-id="b8321-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="b8321-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b8321-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="b8321-119">Devuelve el valor correspondiente al índice de elemento de colección de cadenas, nombre, lenguaje e índice de atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="b8321-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="b8321-120">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="b8321-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="b8321-121">Devuelve un valor que indica si el objeto proporcionado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="b8321-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="b8321-122">Obtenga una interfaz **IWMPStringCollection2** convirtiendo el valor devuelto por el método [**IWMPMediaCollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) .</span><span class="sxs-lookup"><span data-stu-id="b8321-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8321-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8321-123">Requirements</span></span>



| <span data-ttu-id="b8321-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8321-124">Requirement</span></span> | <span data-ttu-id="b8321-125">Value</span><span class="sxs-lookup"><span data-stu-id="b8321-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8321-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8321-126">Header</span></span><br/> | <dl> <span data-ttu-id="b8321-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8321-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8321-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8321-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8321-129">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="b8321-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8321-130">**Interfaz IWMPStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8321-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





