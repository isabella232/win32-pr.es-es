---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076410"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="f6bd2-103">IAgentCharacter::P establecer</span><span class="sxs-lookup"><span data-stu-id="f6bd2-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="f6bd2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6bd2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="f6bd2-105">Reproduce la animación especificada.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="f6bd2-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="f6bd2-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="f6bd2-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span><span class="sxs-lookup"><span data-stu-id="f6bd2-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="f6bd2-109">Nombre de una animación.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="f6bd2-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="f6bd2-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f6bd2-111">Dirección de una variable que recibe el identificador de solicitud **IAgentCharacter::P** .</span><span class="sxs-lookup"><span data-stu-id="f6bd2-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="f6bd2-112">El nombre de una animación se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f6bd2-113">Antes de reproducir la animación especificada, el servidor intenta reproducir la animación de **retorno** de la animación anterior (si se ha asignado alguna).</span><span class="sxs-lookup"><span data-stu-id="f6bd2-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="f6bd2-114">Cuando los datos de animación de un carácter se almacenan en el equipo local del usuario, puede utilizar el método **IAgentCharacter::P establecer** y especificar el nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="f6bd2-115">Al usar el protocolo HTTP para tener acceso a los datos de animación, use el método [**Prepare**](iagentcharacter--prepare.md) para garantizar la disponibilidad de la animación antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="f6bd2-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6bd2-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f6bd2-116">See Also</span></span>

[<span data-ttu-id="f6bd2-117">**IAgentCharacter::P redondear**</span><span class="sxs-lookup"><span data-stu-id="f6bd2-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




