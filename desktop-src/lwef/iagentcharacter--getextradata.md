---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148863"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="4dfc4-103">IAgentCharacter::GetExtraData</span><span class="sxs-lookup"><span data-stu-id="4dfc4-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="4dfc4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4dfc4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="4dfc4-105">Recupera datos adicionales almacenados como parte del carácter.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="4dfc4-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4dfc4-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span><span class="sxs-lookup"><span data-stu-id="4dfc4-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="4dfc4-108">Dirección de un BSTR que recibe el valor de los datos adicionales para el carácter.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="4dfc4-109">Los datos adicionales de un carácter se definen cuando se compilan con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4dfc4-110">Un desarrollador de caracteres puede proporcionar esta cadena editando. Archivo ACD para un carácter.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="4dfc4-111">La configuración es opcional y es posible que no se proporcione para todos los caracteres, ni se pueden definir o cambiar los datos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="4dfc4-112">Además, el significado de los datos proporcionados lo define el desarrollador de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4dfc4-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




