---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419208"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="0ac41-103">IAgentCharacter::GestureAt</span><span class="sxs-lookup"><span data-stu-id="0ac41-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="0ac41-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ac41-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="0ac41-105">Reproduce la animación de estado de **gesturing** asociada en función de la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="0ac41-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="0ac41-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ac41-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="0ac41-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ac41-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="0ac41-108"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="0ac41-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="0ac41-109">Coordenada x de la ubicación especificada en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="0ac41-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="0ac41-110"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="0ac41-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="0ac41-111">Coordenada y de la ubicación especificada en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="0ac41-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="0ac41-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="0ac41-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="0ac41-113">Dirección de una variable que recibe el identificador de solicitud **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="0ac41-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="0ac41-114">El servidor determina y reproduce automáticamente la animación gesturing adecuada según la posición actual del carácter y la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="0ac41-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="0ac41-115">Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](iagentcharacter--prepare.md) para asegurarse de que las animaciones estén disponibles antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="0ac41-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 




