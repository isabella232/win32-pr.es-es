---
title: Controls. Next (método)
description: El método siguiente establece el elemento actual en el elemento siguiente de la lista de reproducción.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- siguiente método de Windows Media Player
- Next Method Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método Next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700355"
---
# <a name="controlsnext-method"></a><span data-ttu-id="32a1b-106">Controls. Next (método)</span><span class="sxs-lookup"><span data-stu-id="32a1b-106">Controls.next method</span></span>

<span data-ttu-id="32a1b-107">El método **siguiente** establece el elemento actual en el elemento siguiente de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="32a1b-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a1b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32a1b-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="32a1b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32a1b-109">Parameters</span></span>

<span data-ttu-id="32a1b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="32a1b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32a1b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32a1b-111">Return value</span></span>

<span data-ttu-id="32a1b-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="32a1b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a1b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32a1b-113">Remarks</span></span>

<span data-ttu-id="32a1b-114">Si la lista de reproducción está en la última entrada cuando se invoca **siguiente** , la primera entrada de la lista de reproducción se convertirá en la actual.</span><span class="sxs-lookup"><span data-stu-id="32a1b-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="32a1b-115">En las listas de reproducción del lado servidor, este método omite el siguiente elemento de la lista de reproducción del servidor, no la lista de reproducción del cliente.</span><span class="sxs-lookup"><span data-stu-id="32a1b-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="32a1b-116">Al reproducir un DVD, este método omite el siguiente capítulo lógico de la secuencia de reproducción, que puede no ser el siguiente capítulo de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="32a1b-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="32a1b-117">Al reproducir DVD todavía, este método pasa al siguiente.</span><span class="sxs-lookup"><span data-stu-id="32a1b-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="32a1b-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="32a1b-118">Examples</span></span>

<span data-ttu-id="32a1b-119">En el ejemplo siguiente se crea un elemento de botón HTML que usa **Next** para moverse al siguiente elemento de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="32a1b-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="32a1b-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="32a1b-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="32a1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32a1b-121">Requirements</span></span>



| <span data-ttu-id="32a1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a1b-122">Requirement</span></span> | <span data-ttu-id="32a1b-123">Value</span><span class="sxs-lookup"><span data-stu-id="32a1b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32a1b-124">Versión</span><span class="sxs-lookup"><span data-stu-id="32a1b-124">Version</span></span><br/> | <span data-ttu-id="32a1b-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="32a1b-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="32a1b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32a1b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="32a1b-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a1b-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a1b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="32a1b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a1b-129">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="32a1b-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="32a1b-130">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="32a1b-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="32a1b-131">**Controls. STOP**</span><span class="sxs-lookup"><span data-stu-id="32a1b-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





