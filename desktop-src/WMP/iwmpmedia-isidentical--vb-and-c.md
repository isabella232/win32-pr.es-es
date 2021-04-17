---
title: IWMPMedia. isIdentical (VB y C)
description: La propiedad isIdentical (el \_ método get isIdentical de C \) obtiene un valor que indica si el elemento multimedia especificado es igual que el actual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690771"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="18a73-104">IWMPMedia. isIdentical (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="18a73-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="18a73-105">La propiedad **isIdentical** (el método **Get \_ isIdentical** en C#) obtiene un valor que indica si el elemento multimedia especificado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="18a73-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="18a73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18a73-106">Parameters</span></span>

<span data-ttu-id="18a73-107">*pIWMPMedia*</span><span class="sxs-lookup"><span data-stu-id="18a73-107">*pIWMPMedia*</span></span>

<span data-ttu-id="18a73-108">Una interfaz **WMPLib. IWMPMedia** para el elemento multimedia que se va a comparar con el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="18a73-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="18a73-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="18a73-109">Property Value</span></span>

<span data-ttu-id="18a73-110">Valor **System. Boolean** que indica si los dos elementos multimedia son idénticos.</span><span class="sxs-lookup"><span data-stu-id="18a73-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="18a73-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18a73-111">Remarks</span></span>

<span data-ttu-id="18a73-112">**IWMPMedia. isIdentical** es una propiedad de Visual Basic que toma un parámetro.</span><span class="sxs-lookup"><span data-stu-id="18a73-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="18a73-113">En C#, se hace referencia a él como el método **IWMPMedia. Get \_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="18a73-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="18a73-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="18a73-114">Examples</span></span>

<span data-ttu-id="18a73-115">En el ejemplo siguiente se usa la propiedad **isIdentical** (el método **Get \_ isIdentical** en C#) para comprobar si un elemento multimedia denominado newMedia es igual que el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="18a73-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="18a73-116">Si no son iguales, se reproduce el nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="18a73-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="18a73-117">De lo contrario, el medio actual sigue reproduciéndose sin interrupciones.</span><span class="sxs-lookup"><span data-stu-id="18a73-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="18a73-118">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="18a73-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="18a73-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18a73-119">Requirements</span></span>



| <span data-ttu-id="18a73-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a73-120">Requirement</span></span> | <span data-ttu-id="18a73-121">Value</span><span class="sxs-lookup"><span data-stu-id="18a73-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a73-122">Versión</span><span class="sxs-lookup"><span data-stu-id="18a73-122">Version</span></span><br/>   | <span data-ttu-id="18a73-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="18a73-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="18a73-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="18a73-124">Namespace</span></span><br/> | <span data-ttu-id="18a73-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="18a73-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18a73-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="18a73-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18a73-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18a73-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a73-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="18a73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a73-129">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="18a73-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





