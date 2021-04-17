---
title: AxWindowsMediaPlayer. Close (método)
description: El método Close cierra el archivo multimedia digital actual, detiene la reproducción en Windows Media Player y libera los recursos de Windows Media Player.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- Close (método) de Windows Media Player
- Close (método) de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699572"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="778ae-106">AxWindowsMediaPlayer. Close (método)</span><span class="sxs-lookup"><span data-stu-id="778ae-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="778ae-107">El método Close cierra el archivo multimedia digital actual, detiene la reproducción en Windows Media Player y libera los recursos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="778ae-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="778ae-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="778ae-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="778ae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="778ae-109">Parameters</span></span>

<span data-ttu-id="778ae-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="778ae-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="778ae-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="778ae-111">Return value</span></span>

<span data-ttu-id="778ae-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="778ae-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="778ae-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="778ae-113">Remarks</span></span>

<span data-ttu-id="778ae-114">Este método cierra el archivo multimedia digital actual, no Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="778ae-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="778ae-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="778ae-115">Examples</span></span>

<span data-ttu-id="778ae-116">En el ejemplo siguiente se crea un botón que, al hacer clic en él, detiene la reproducción en Windows Media Player y libera los recursos en uso.</span><span class="sxs-lookup"><span data-stu-id="778ae-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="778ae-117">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="778ae-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="778ae-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="778ae-118">Requirements</span></span>



| <span data-ttu-id="778ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="778ae-119">Requirement</span></span> | <span data-ttu-id="778ae-120">Value</span><span class="sxs-lookup"><span data-stu-id="778ae-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="778ae-121">Versión</span><span class="sxs-lookup"><span data-stu-id="778ae-121">Version</span></span><br/>   | <span data-ttu-id="778ae-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="778ae-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="778ae-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="778ae-123">Namespace</span></span><br/> | <span data-ttu-id="778ae-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="778ae-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="778ae-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="778ae-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="778ae-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="778ae-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778ae-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="778ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778ae-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="778ae-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





