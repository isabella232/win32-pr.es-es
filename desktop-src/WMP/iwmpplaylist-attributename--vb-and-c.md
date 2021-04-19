---
title: IWMPPlaylist. attributeName (VB y C)
description: La propiedad attributeName (el \_ método get attributeName en C \) obtiene el nombre de un atributo de lista de reproducción especificado por un índice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689959"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="c9789-104">IWMPPlaylist. attributeName (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="c9789-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="c9789-105">La propiedad **attributeName** (el método **Get \_ attributeName** en C#) obtiene el nombre de un atributo de lista de reproducción especificado por un índice.</span><span class="sxs-lookup"><span data-stu-id="c9789-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c9789-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9789-106">Parameters</span></span>

<span data-ttu-id="c9789-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="c9789-107">*lIndex*</span></span>

<span data-ttu-id="c9789-108">**System. Int32** que es el índice del atributo de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c9789-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9789-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9789-109">Return Value</span></span>

<span data-ttu-id="c9789-110">**System. String** que es el nombre del atributo de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c9789-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9789-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9789-111">Remarks</span></span>

<span data-ttu-id="c9789-112">**IWMPPlaylist. attributeName** es una propiedad de solo lectura en Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist. Get \_ attributeName** .</span><span class="sxs-lookup"><span data-stu-id="c9789-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="c9789-113">La propiedad **IWMPPlaylist. attributeCount** devuelve el número de atributos asociado a una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c9789-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="c9789-114">El nombre devuelto por esta propiedad se puede proporcionar a los métodos **setItemInfo** o **getItemInfo** para especificar o recuperar un valor para el atributo con nombre.</span><span class="sxs-lookup"><span data-stu-id="c9789-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="c9789-115">Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c9789-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="c9789-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c9789-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c9789-117">Para obtener más información sobre los atributos compatibles con Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c9789-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c9789-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c9789-118">Examples</span></span>

<span data-ttu-id="c9789-119">Vea la propiedad [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9789-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9789-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9789-120">Requirements</span></span>



| <span data-ttu-id="c9789-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9789-121">Requirement</span></span> | <span data-ttu-id="c9789-122">Value</span><span class="sxs-lookup"><span data-stu-id="c9789-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9789-123">Versión</span><span class="sxs-lookup"><span data-stu-id="c9789-123">Version</span></span><br/>   | <span data-ttu-id="c9789-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c9789-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c9789-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9789-125">Namespace</span></span><br/> | <span data-ttu-id="c9789-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c9789-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c9789-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c9789-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c9789-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c9789-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9789-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9789-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9789-130">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9789-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9789-131">**IWMPPlaylist. attributeCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9789-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9789-132">**IWMPPlaylist. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9789-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9789-133">**IWMPPlaylist. setItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9789-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





