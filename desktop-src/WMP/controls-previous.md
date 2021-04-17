---
title: Controls. Previous (método)
description: El método anterior establece el elemento actual en el elemento anterior de la lista de reproducción.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- método anterior de Windows Media Player
- método anterior Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método Previous
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699899"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="28655-106">Controls. Previous (método)</span><span class="sxs-lookup"><span data-stu-id="28655-106">Controls.previous method</span></span>

<span data-ttu-id="28655-107">El método **anterior** establece el elemento actual en el elemento anterior de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="28655-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="28655-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28655-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="28655-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28655-109">Parameters</span></span>

<span data-ttu-id="28655-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28655-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28655-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28655-111">Return value</span></span>

<span data-ttu-id="28655-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28655-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28655-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28655-113">Remarks</span></span>

<span data-ttu-id="28655-114">Si la lista de reproducción está en la primera entrada cuando se invoca el **anterior** , la última entrada de la lista de reproducción se convertirá en la actual.</span><span class="sxs-lookup"><span data-stu-id="28655-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="28655-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="28655-115">Examples</span></span>

<span data-ttu-id="28655-116">En el ejemplo siguiente se crea un elemento de botón HTML que utiliza **Previous** para moverse al elemento anterior de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="28655-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="28655-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="28655-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="28655-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28655-118">Requirements</span></span>



| <span data-ttu-id="28655-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28655-119">Requirement</span></span> | <span data-ttu-id="28655-120">Value</span><span class="sxs-lookup"><span data-stu-id="28655-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28655-121">Versión</span><span class="sxs-lookup"><span data-stu-id="28655-121">Version</span></span><br/> | <span data-ttu-id="28655-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="28655-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="28655-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28655-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="28655-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28655-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28655-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="28655-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28655-126">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="28655-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="28655-127">**Controls. Next**</span><span class="sxs-lookup"><span data-stu-id="28655-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="28655-128">**Controls. STOP**</span><span class="sxs-lookup"><span data-stu-id="28655-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





