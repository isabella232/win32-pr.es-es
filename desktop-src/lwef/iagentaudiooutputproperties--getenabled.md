---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075680"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="e06a5-103">IAgentAudioOutputProperties::GetEnabled</span><span class="sxs-lookup"><span data-stu-id="e06a5-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="e06a5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e06a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="e06a5-105">Recupera un valor que indica si la salida de voz de caracteres está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e06a5-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="e06a5-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e06a5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e06a5-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="e06a5-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="e06a5-108">Dirección de una variable que recibe **true** si la salida de voz está habilitada actualmente y **false** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e06a5-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="e06a5-109">Dado que esta configuración afecta a la salida de voz (TTS y el archivo de sonido) de todos los caracteres, solo el usuario puede cambiar esta propiedad en la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e06a5-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




