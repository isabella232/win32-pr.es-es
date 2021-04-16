---
title: Propiedad AxWindowsMediaPlayer. stretchToFit
description: La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- propiedades de stretchToFit Media Player de Windows
- propiedad stretchToFit Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699956"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="a5152-106">Propiedad AxWindowsMediaPlayer. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="a5152-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="a5152-107">La propiedad stretchToFit obtiene o establece un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5152-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5152-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5152-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="a5152-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a5152-109">Property value</span></span>

<span data-ttu-id="a5152-110">El valor System. Boolean que indica si el vídeo se ajustará para ajustarse a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5152-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="a5152-111">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a5152-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5152-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5152-112">Remarks</span></span>

<span data-ttu-id="a5152-113">Cuando **stretchToFit** se establece en true, el control de Media Player de Windows mantiene la relación de aspecto original del vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5152-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="a5152-114">Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, pueden aparecer áreas de máscara negra en la parte superior e inferior, o izquierda y derecha, de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5152-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="a5152-115">Esta propiedad solo se aplica al control Media Player de Windows cuando se incrusta en una página web.</span><span class="sxs-lookup"><span data-stu-id="a5152-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5152-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5152-116">Requirements</span></span>



| <span data-ttu-id="a5152-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5152-117">Requirement</span></span> | <span data-ttu-id="a5152-118">Value</span><span class="sxs-lookup"><span data-stu-id="a5152-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5152-119">Versión</span><span class="sxs-lookup"><span data-stu-id="a5152-119">Version</span></span><br/>   | <span data-ttu-id="a5152-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a5152-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a5152-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5152-121">Namespace</span></span><br/> | <span data-ttu-id="a5152-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a5152-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a5152-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a5152-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5152-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a5152-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5152-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5152-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5152-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5152-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





