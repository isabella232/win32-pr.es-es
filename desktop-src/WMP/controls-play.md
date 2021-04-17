---
title: Controls. Play (método)
description: El método play hace que el elemento multimedia actual empiece a reproducir o reanuda la reproducción de un elemento pausado.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- método play Windows Media Player
- método play Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700035"
---
# <a name="controlsplay-method"></a><span data-ttu-id="cd7fa-106">Controls. Play (método)</span><span class="sxs-lookup"><span data-stu-id="cd7fa-106">Controls.play method</span></span>

<span data-ttu-id="cd7fa-107">El método **Play** hace que el elemento multimedia actual empiece a reproducir o reanuda la reproducción de un elemento pausado.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7fa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd7fa-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="cd7fa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd7fa-109">Parameters</span></span>

<span data-ttu-id="cd7fa-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd7fa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd7fa-111">Return value</span></span>

<span data-ttu-id="cd7fa-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7fa-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd7fa-113">Remarks</span></span>

<span data-ttu-id="cd7fa-114">Si se llama a este método durante el reenvío rápido o el rebobinado, el valor de *Settings*. la **velocidad** se establece en 1,0.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="cd7fa-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cd7fa-115">Examples</span></span>

<span data-ttu-id="cd7fa-116">En el ejemplo siguiente se crea un elemento de botón HTML que utiliza **Play** para reproducir el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="cd7fa-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cd7fa-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="cd7fa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd7fa-118">Requirements</span></span>



| <span data-ttu-id="cd7fa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7fa-119">Requirement</span></span> | <span data-ttu-id="cd7fa-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd7fa-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7fa-121">Versión</span><span class="sxs-lookup"><span data-stu-id="cd7fa-121">Version</span></span><br/> | <span data-ttu-id="cd7fa-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cd7fa-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cd7fa-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd7fa-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd7fa-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd7fa-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7fa-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd7fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7fa-126">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="cd7fa-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





