---
title: Player. Close (método)
description: El método Close libera los recursos de Media Player de Windows.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Close (método) de Windows Media Player
- Close (método) Windows Media Player, clase Player
- Clase player Windows Media Player, Close (método)
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699850"
---
# <a name="playerclose-method"></a><span data-ttu-id="ed4cc-106">Player. Close (método)</span><span class="sxs-lookup"><span data-stu-id="ed4cc-106">Player.close method</span></span>

<span data-ttu-id="ed4cc-107">El método **Close** libera los recursos de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed4cc-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="ed4cc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed4cc-109">Parameters</span></span>

<span data-ttu-id="ed4cc-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed4cc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed4cc-111">Return value</span></span>

<span data-ttu-id="ed4cc-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed4cc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed4cc-113">Remarks</span></span>

<span data-ttu-id="ed4cc-114">Este método cierra el archivo multimedia digital actual, no Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="ed4cc-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed4cc-115">Examples</span></span>

<span data-ttu-id="ed4cc-116">En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, detiene la reproducción en Windows Media Player y libera los recursos en uso.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="ed4cc-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ed4cc-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="ed4cc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4cc-118">Requirements</span></span>



| <span data-ttu-id="ed4cc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4cc-119">Requirement</span></span> | <span data-ttu-id="ed4cc-120">Value</span><span class="sxs-lookup"><span data-stu-id="ed4cc-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4cc-121">Versión</span><span class="sxs-lookup"><span data-stu-id="ed4cc-121">Version</span></span><br/> | <span data-ttu-id="ed4cc-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ed4cc-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed4cc-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed4cc-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4cc-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4cc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed4cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4cc-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="ed4cc-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





