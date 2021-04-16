---
title: Propiedad AxWindowsMediaPlayer. status
description: La propiedad status obtiene un valor que indica el estado de Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- propiedades de estado de Windows Media Player
- propiedad status Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699703"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="63846-106">Propiedad AxWindowsMediaPlayer. status</span><span class="sxs-lookup"><span data-stu-id="63846-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="63846-107">La propiedad status obtiene un valor que indica el estado de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="63846-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="63846-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63846-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63846-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63846-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="63846-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63846-110">Property value</span></span>

<span data-ttu-id="63846-111">System. String que es el estado.</span><span class="sxs-lookup"><span data-stu-id="63846-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="63846-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63846-112">Remarks</span></span>

<span data-ttu-id="63846-113">Los valores contenidos en esta propiedad están sujetos a cambios en cualquier momento y deben usarse solo con fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="63846-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="63846-114">AxWindowsMediaPlayer. El evento **StatusChange** se desencadena cuando esta propiedad cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="63846-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="63846-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63846-115">Requirements</span></span>



| <span data-ttu-id="63846-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63846-116">Requirement</span></span> | <span data-ttu-id="63846-117">Value</span><span class="sxs-lookup"><span data-stu-id="63846-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63846-118">Versión</span><span class="sxs-lookup"><span data-stu-id="63846-118">Version</span></span><br/>   | <span data-ttu-id="63846-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="63846-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="63846-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63846-120">Namespace</span></span><br/> | <span data-ttu-id="63846-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="63846-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="63846-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="63846-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="63846-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="63846-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63846-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="63846-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63846-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="63846-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="63846-126">**Evento AxWindowsMediaPlayer. StatusChange (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="63846-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





