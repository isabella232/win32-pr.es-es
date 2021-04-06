---
title: IAgentCharacter Mostrar
description: IAgentCharacter Mostrar
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077755"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="ef099-103">IAgentCharacter:: show</span><span class="sxs-lookup"><span data-stu-id="ef099-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="ef099-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef099-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="ef099-105">Muestra un carácter.</span><span class="sxs-lookup"><span data-stu-id="ef099-105">Displays a character.</span></span>

-   <span data-ttu-id="ef099-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef099-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="ef099-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef099-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="ef099-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="ef099-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="ef099-109">Marca de animación de estado que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ef099-109">Showing state animation flag.</span></span> <span data-ttu-id="ef099-110">Si este parámetro es **true**, la animación de estado **que** se reproduce después de que el carácter esté visible; Si **es false**, la animación no se reproduce.</span><span class="sxs-lookup"><span data-stu-id="ef099-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="ef099-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="ef099-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="ef099-112">Dirección de una variable que recibe el identificador de solicitud de [**presentación**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="ef099-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="ef099-113">Evite establecer el parámetro *bFast* en **true** sin reproducir una animación de antemano; de lo contrario, se puede mostrar el marco de caracteres, pero no tiene ninguna imagen para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ef099-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="ef099-114">En concreto, tenga en cuenta que si llama a [**moveTo**](iagentcharacter--moveto.md) cuando el carácter no está visible, no se reproduce ninguna animación.</span><span class="sxs-lookup"><span data-stu-id="ef099-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="ef099-115">Por lo tanto, si llama al método **Show** con *BFAST* establecido en **true**, no se mostrará ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="ef099-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="ef099-116">Del mismo modo, si llama a [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), **Show** with *bFast* establecido en **true**, no habrá ninguna imagen visible.</span><span class="sxs-lookup"><span data-stu-id="ef099-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="ef099-117">Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de la animación de estado **que se muestra** antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="ef099-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef099-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ef099-118">See Also</span></span>

[<span data-ttu-id="ef099-119">**IAgentCharacter:: Hide**</span><span class="sxs-lookup"><span data-stu-id="ef099-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 