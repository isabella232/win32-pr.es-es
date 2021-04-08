---
title: IAgentCharacter moveTo
description: IAgentCharacter moveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077627"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="47c39-103">IAgentCharacter:: moveTo</span><span class="sxs-lookup"><span data-stu-id="47c39-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="47c39-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47c39-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="47c39-105">Reproduce la animación de estado de **movimiento** asociada y mueve el marco de caracteres a la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="47c39-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="47c39-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="47c39-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="47c39-107">Cuando la función devuelve, esta variable contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47c39-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="47c39-108"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="47c39-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="47c39-109">Coordenada x de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="47c39-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="47c39-110">La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.</span><span class="sxs-lookup"><span data-stu-id="47c39-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="47c39-111"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="47c39-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="47c39-112">Coordenada y de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="47c39-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="47c39-113">La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.</span><span class="sxs-lookup"><span data-stu-id="47c39-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="47c39-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span><span class="sxs-lookup"><span data-stu-id="47c39-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="47c39-115">Parámetro que especifica en milisegundos la rapidez con la que se mueve el marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="47c39-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="47c39-116">El valor recomendado es 1000.</span><span class="sxs-lookup"><span data-stu-id="47c39-116">The recommended value is 1000.</span></span> <span data-ttu-id="47c39-117">Si se especifica cero (0), se mueve el marco sin reproducir una animación.</span><span class="sxs-lookup"><span data-stu-id="47c39-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="47c39-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="47c39-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="47c39-119">Dirección de una variable que recibe el identificador de solicitud [**moveTo**](https://www.bing.com/search?q=**MoveTo**) .</span><span class="sxs-lookup"><span data-stu-id="47c39-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="47c39-120">Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de las animaciones de estado en **movimiento** antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="47c39-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="47c39-121">Incluso si la animación no está cargada, el servidor todavía mueve el marco.</span><span class="sxs-lookup"><span data-stu-id="47c39-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="47c39-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47c39-122">See Also</span></span>

[<span data-ttu-id="47c39-123">**IAgentCharacter:: SetPosition**</span><span class="sxs-lookup"><span data-stu-id="47c39-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 