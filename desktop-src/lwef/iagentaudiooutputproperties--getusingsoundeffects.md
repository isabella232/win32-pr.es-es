---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776176"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="825b9-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span><span class="sxs-lookup"><span data-stu-id="825b9-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="825b9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="825b9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="825b9-105">Recupera un valor que indica si la salida de efectos sonoros está habilitada.</span><span class="sxs-lookup"><span data-stu-id="825b9-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="825b9-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="825b9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="825b9-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span><span class="sxs-lookup"><span data-stu-id="825b9-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="825b9-108">Dirección de una variable que recibe **true** si la salida de efectos de sonido está habilitada actualmente y **false** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="825b9-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="825b9-109">Los efectos sonoros de la animación de un carácter se asignan en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="825b9-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="825b9-110">Dado que esta configuración afecta a la salida de efectos sonoros de todos los caracteres, solo el usuario puede cambiar esta propiedad en la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="825b9-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




