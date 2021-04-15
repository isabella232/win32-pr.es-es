---
title: Settings. MUTE
description: La propiedad MUTE especifica y recupera un valor que indica si el audio está silenciado.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Configuración. silenciar Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708800"
---
# <a name="settingsmute"></a><span data-ttu-id="5c858-104">Settings. MUTE</span><span class="sxs-lookup"><span data-stu-id="5c858-104">Settings.mute</span></span>

<span data-ttu-id="5c858-105">La propiedad **MUTE** especifica y recupera un valor que indica si el audio está silenciado.</span><span class="sxs-lookup"><span data-stu-id="5c858-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c858-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c858-106">Syntax</span></span>

<span data-ttu-id="5c858-107">Player. Settings. MUTE</span><span class="sxs-lookup"><span data-stu-id="5c858-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="5c858-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5c858-108">Possible Values</span></span>

<span data-ttu-id="5c858-109">Esta propiedad es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="5c858-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5c858-110">Value</span><span class="sxs-lookup"><span data-stu-id="5c858-110">Value</span></span> | <span data-ttu-id="5c858-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c858-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="5c858-112">true</span><span class="sxs-lookup"><span data-stu-id="5c858-112">true</span></span>  | <span data-ttu-id="5c858-113">El audio está silenciado.</span><span class="sxs-lookup"><span data-stu-id="5c858-113">Audio is muted.</span></span>              |
| <span data-ttu-id="5c858-114">false</span><span class="sxs-lookup"><span data-stu-id="5c858-114">false</span></span> | <span data-ttu-id="5c858-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5c858-115">Default.</span></span> <span data-ttu-id="5c858-116">Audio no silenciado.</span><span class="sxs-lookup"><span data-stu-id="5c858-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="5c858-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5c858-117">Examples</span></span>

<span data-ttu-id="5c858-118">En el ejemplo siguiente se crea un elemento CHECKBOX HTML que permite al usuario silenciar y deshacer el audio.</span><span class="sxs-lookup"><span data-stu-id="5c858-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="5c858-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5c858-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="5c858-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c858-120">Requirements</span></span>



| <span data-ttu-id="5c858-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c858-121">Requirement</span></span> | <span data-ttu-id="5c858-122">Value</span><span class="sxs-lookup"><span data-stu-id="5c858-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c858-123">Versión</span><span class="sxs-lookup"><span data-stu-id="5c858-123">Version</span></span><br/> | <span data-ttu-id="5c858-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5c858-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5c858-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c858-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c858-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c858-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c858-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c858-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c858-128">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="5c858-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





