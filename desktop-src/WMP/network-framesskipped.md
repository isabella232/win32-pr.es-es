---
title: Network. framesSkipped
description: La propiedad framesSkipped recupera el número total de fotogramas omitidos durante la reproducción.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Windows Media Player de red. framesSkipped
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708971"
---
# <a name="networkframesskipped"></a><span data-ttu-id="4bbf1-104">Network. framesSkipped</span><span class="sxs-lookup"><span data-stu-id="4bbf1-104">Network.framesSkipped</span></span>

<span data-ttu-id="4bbf1-105">La propiedad **framesSkipped** recupera el número total de fotogramas omitidos durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bbf1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bbf1-106">Syntax</span></span>

<span data-ttu-id="4bbf1-107">*reproductor*. *red*. **framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="4bbf1-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4bbf1-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4bbf1-108">Possible Values</span></span>

<span data-ttu-id="4bbf1-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4bbf1-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="4bbf1-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4bbf1-110">Examples</span></span>

<span data-ttu-id="4bbf1-111">En el siguiente ejemplo de JScript se usa *Network*. **framesSkipped** para mostrar el número total de fotogramas omitidos durante la reproducción cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="4bbf1-112">La información se muestra en un DIV HTML creado con ID = "FS".</span><span class="sxs-lookup"><span data-stu-id="4bbf1-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="4bbf1-113">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4bbf1-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="4bbf1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bbf1-114">Requirements</span></span>



| <span data-ttu-id="4bbf1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bbf1-115">Requirement</span></span> | <span data-ttu-id="4bbf1-116">Value</span><span class="sxs-lookup"><span data-stu-id="4bbf1-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbf1-117">Versión</span><span class="sxs-lookup"><span data-stu-id="4bbf1-117">Version</span></span><br/> | <span data-ttu-id="4bbf1-118">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4bbf1-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bbf1-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4bbf1-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bbf1-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bbf1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bbf1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bbf1-122">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="4bbf1-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





