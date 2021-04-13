---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357720"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="06618-103">IAgentBalloon::GetEnabled</span><span class="sxs-lookup"><span data-stu-id="06618-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="06618-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="06618-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="06618-105">Recupera el valor de la propiedad [**Enabled**](enabled-property.md) de un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="06618-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="06618-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="06618-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="06618-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="06618-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="06618-108">La dirección de una variable que recibe **true** cuando el globo de palabras está habilitado y **false** cuando está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="06618-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="06618-109">El servidor de Microsoft Agent muestra automáticamente el globo de palabras para la salida de voz, a menos que esté deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="06618-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="06618-110">El globo de palabras se puede deshabilitar para un carácter en el editor de caracteres del agente de Microsoft o (por el usuario) para todos los caracteres de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06618-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="06618-111">Si el usuario deshabilita el globo de palabras, el cliente no podrá restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="06618-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




