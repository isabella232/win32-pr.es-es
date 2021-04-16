---
title: Propiedad AxWindowsMediaPlayer. openState
description: La propiedad openState obtiene un valor de enumeración que indica el estado del origen de contenido.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- propiedades de openState Media Player de Windows
- propiedad openState Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699392"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="e8fd1-106">Propiedad AxWindowsMediaPlayer. openState</span><span class="sxs-lookup"><span data-stu-id="e8fd1-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="e8fd1-107">La propiedad openState obtiene un valor de enumeración que indica el estado del origen de contenido.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="e8fd1-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fd1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8fd1-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="e8fd1-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8fd1-110">Property value</span></span>

<span data-ttu-id="e8fd1-111">El valor de enumeración WMPLib. WMPOpenState.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fd1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8fd1-112">Remarks</span></span>

<span data-ttu-id="e8fd1-113">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="e8fd1-114">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="e8fd1-115">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8fd1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8fd1-116">Requirements</span></span>



| <span data-ttu-id="e8fd1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8fd1-117">Requirement</span></span> | <span data-ttu-id="e8fd1-118">Value</span><span class="sxs-lookup"><span data-stu-id="e8fd1-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fd1-119">Versión</span><span class="sxs-lookup"><span data-stu-id="e8fd1-119">Version</span></span><br/>   | <span data-ttu-id="e8fd1-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e8fd1-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e8fd1-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8fd1-121">Namespace</span></span><br/> | <span data-ttu-id="e8fd1-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e8fd1-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e8fd1-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e8fd1-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e8fd1-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8fd1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8fd1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fd1-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8fd1-127">**Evento AxWindowsMediaPlayer. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="e8fd1-128">**WMPLib.WMPOpenState**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





