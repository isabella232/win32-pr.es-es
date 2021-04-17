---
title: Propiedad AxWindowsMediaPlayer. mediaCollection
description: La propiedad mediaCollection obtiene una interfaz IWMPMediaCollection que proporciona una manera de organizar una colección grande de elementos multimedia.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- propiedades de mediaCollection Media Player de Windows
- propiedad mediaCollection Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad mediaCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700156"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="16b04-106">Propiedad AxWindowsMediaPlayer. mediaCollection</span><span class="sxs-lookup"><span data-stu-id="16b04-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="16b04-107">La propiedad mediaCollection obtiene una interfaz **IWMPMediaCollection** que proporciona una manera de organizar una colección grande de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="16b04-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="16b04-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16b04-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16b04-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="16b04-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="16b04-110">Property value</span></span>

<span data-ttu-id="16b04-111">La interfaz WMPLib. IWMPMediaCollection para una colección de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="16b04-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b04-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16b04-112">Remarks</span></span>

<span data-ttu-id="16b04-113">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="16b04-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="16b04-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="16b04-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16b04-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b04-115">Requirements</span></span>



| <span data-ttu-id="16b04-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b04-116">Requirement</span></span> | <span data-ttu-id="16b04-117">Value</span><span class="sxs-lookup"><span data-stu-id="16b04-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b04-118">Versión</span><span class="sxs-lookup"><span data-stu-id="16b04-118">Version</span></span><br/>   | <span data-ttu-id="16b04-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="16b04-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16b04-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="16b04-120">Namespace</span></span><br/> | <span data-ttu-id="16b04-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="16b04-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16b04-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="16b04-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16b04-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="16b04-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b04-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="16b04-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b04-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16b04-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16b04-126">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16b04-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16b04-127">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16b04-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16b04-128">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="16b04-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





