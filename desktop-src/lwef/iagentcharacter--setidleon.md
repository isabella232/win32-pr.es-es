---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419198"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="21487-103">IAgentCharacter::SetIdleOn</span><span class="sxs-lookup"><span data-stu-id="21487-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="21487-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="21487-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="21487-105">Establece el procesamiento de inactividad automático para un carácter.</span><span class="sxs-lookup"><span data-stu-id="21487-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="21487-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="21487-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="21487-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Despedida*</span><span class="sxs-lookup"><span data-stu-id="21487-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="21487-108">Marca de procesamiento inactivo.</span><span class="sxs-lookup"><span data-stu-id="21487-108">Idle processing flag.</span></span> <span data-ttu-id="21487-109">Si este parámetro es **true**, el agente de Microsoft reproduce automáticamente las animaciones de estado de **ralentí** .</span><span class="sxs-lookup"><span data-stu-id="21487-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="21487-110">El servidor establece automáticamente un tiempo de espera después de la última animación reproducida para un carácter.</span><span class="sxs-lookup"><span data-stu-id="21487-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="21487-111">Una vez completado el intervalo de este temporizador, el servidor inicia los Estados de **ralentí** para un carácter, reproduciendo sus animaciones de inactiva **asociadas a intervalos** regulares.</span><span class="sxs-lookup"><span data-stu-id="21487-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="21487-112">Si desea administrar las animaciones de estado de **ralentí** , establezca la propiedad en **false**.</span><span class="sxs-lookup"><span data-stu-id="21487-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="21487-113">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="21487-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="21487-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="21487-114">See Also</span></span>

[<span data-ttu-id="21487-115">**IAgentCharacter::GetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="21487-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




