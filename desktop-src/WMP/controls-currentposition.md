---
title: Controls. currentPosition
description: La propiedad currentPosition especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Media Player de Windows Controls. currentPosition
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700131"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="69061-104">Controls. currentPosition</span><span class="sxs-lookup"><span data-stu-id="69061-104">Controls.currentPosition</span></span>

<span data-ttu-id="69061-105">La propiedad **currentPosition** especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.</span><span class="sxs-lookup"><span data-stu-id="69061-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="69061-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="69061-106">Possible Values</span></span>

<span data-ttu-id="69061-107">Esta propiedad es un **número** de lectura/escritura (**Double**).</span><span class="sxs-lookup"><span data-stu-id="69061-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="69061-108">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="69061-108">Examples</span></span>

<span data-ttu-id="69061-109">En el ejemplo siguiente se usa **currentPosition** para buscar una posición proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="69061-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="69061-110">Se crea un elemento de botón HTML para ejecutar el código JScript.</span><span class="sxs-lookup"><span data-stu-id="69061-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="69061-111">Se creó un elemento de entrada de texto HTML, denominado setPosition, para aceptar un valor, en segundos, del usuario.</span><span class="sxs-lookup"><span data-stu-id="69061-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="69061-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="69061-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="69061-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69061-113">Requirements</span></span>



| <span data-ttu-id="69061-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="69061-114">Requirement</span></span> | <span data-ttu-id="69061-115">Value</span><span class="sxs-lookup"><span data-stu-id="69061-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69061-116">Versión</span><span class="sxs-lookup"><span data-stu-id="69061-116">Version</span></span><br/> | <span data-ttu-id="69061-117">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="69061-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="69061-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69061-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="69061-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69061-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69061-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="69061-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69061-121">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="69061-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





