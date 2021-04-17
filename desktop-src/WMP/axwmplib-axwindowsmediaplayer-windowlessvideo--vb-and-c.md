---
title: Propiedad AxWindowsMediaPlayer. windowlessVideo
description: La propiedad windowlessVideo obtiene o establece un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- propiedades de windowlessVideo Media Player de Windows
- propiedad windowlessVideo Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700392"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="74b8c-106">Propiedad AxWindowsMediaPlayer. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="74b8c-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="74b8c-107">La propiedad windowlessVideo obtiene o establece un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="74b8c-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b8c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74b8c-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="74b8c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="74b8c-109">Property value</span></span>

<span data-ttu-id="74b8c-110">Un valor System. Boolean que indica si el control de Media Player de Windows representa el vídeo en modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="74b8c-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="74b8c-111">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="74b8c-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b8c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74b8c-112">Remarks</span></span>

<span data-ttu-id="74b8c-113">De forma predeterminada, un control incrustado de Windows Media Player representa el vídeo en su propia ventana dentro del área cliente.</span><span class="sxs-lookup"><span data-stu-id="74b8c-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="74b8c-114">Cuando **windowlessVideo** se establece en true, el objeto de Media Player de Windows representa el vídeo directamente en el área de cliente, de modo que puede aplicar efectos especiales o capas del vídeo con texto.</span><span class="sxs-lookup"><span data-stu-id="74b8c-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="74b8c-115">En Windows Vista, la representación de vídeo en el modo sin ventanas puede degradar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="74b8c-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="74b8c-116">La obtención de un valor para esta propiedad no es compatible con Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="74b8c-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="74b8c-117">Establecer un valor para esta propiedad en Netscape Navigator puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="74b8c-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b8c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b8c-118">Requirements</span></span>



| <span data-ttu-id="74b8c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b8c-119">Requirement</span></span> | <span data-ttu-id="74b8c-120">Value</span><span class="sxs-lookup"><span data-stu-id="74b8c-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b8c-121">Versión</span><span class="sxs-lookup"><span data-stu-id="74b8c-121">Version</span></span><br/>   | <span data-ttu-id="74b8c-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="74b8c-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="74b8c-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74b8c-123">Namespace</span></span><br/> | <span data-ttu-id="74b8c-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="74b8c-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="74b8c-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="74b8c-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="74b8c-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="74b8c-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b8c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="74b8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b8c-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="74b8c-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





