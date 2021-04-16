---
title: AxWindowsMediaPlayer. openPlayer, método
description: El método openPlayer abre Windows Media Player mediante la dirección URL especificada. | AxWindowsMediaPlayer. openPlayer, método
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- método openPlayer de Windows Media Player
- método openPlayer de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699398"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="ad35e-107">AxWindowsMediaPlayer. openPlayer, método</span><span class="sxs-lookup"><span data-stu-id="ad35e-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="ad35e-108">El método **openPlayer** abre Windows Media Player mediante la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="ad35e-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad35e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad35e-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="ad35e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad35e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad35e-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="ad35e-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="ad35e-112">**System. String** que es la dirección URL del elemento multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="ad35e-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad35e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad35e-113">Return value</span></span>

<span data-ttu-id="ad35e-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ad35e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad35e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad35e-115">Remarks</span></span>

<span data-ttu-id="ad35e-116">Este método inicia Windows Media Player con la dirección URL especificada como elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="ad35e-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="ad35e-117">Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ad35e-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="ad35e-118">De lo contrario, el reproductor se abre en modo completo.</span><span class="sxs-lookup"><span data-stu-id="ad35e-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad35e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad35e-119">Requirements</span></span>



| <span data-ttu-id="ad35e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad35e-120">Requirement</span></span> | <span data-ttu-id="ad35e-121">Value</span><span class="sxs-lookup"><span data-stu-id="ad35e-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad35e-122">Versión</span><span class="sxs-lookup"><span data-stu-id="ad35e-122">Version</span></span><br/>   | <span data-ttu-id="ad35e-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ad35e-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ad35e-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad35e-124">Namespace</span></span><br/> | <span data-ttu-id="ad35e-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ad35e-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ad35e-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ad35e-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ad35e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ad35e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad35e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad35e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad35e-129">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ad35e-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





