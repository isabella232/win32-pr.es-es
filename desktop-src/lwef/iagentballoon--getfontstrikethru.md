---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419110"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="dc1b4-103">IAgentBalloon::GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="dc1b4-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="dc1b4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc1b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="dc1b4-105">Indica si la fuente utilizada en un globo de palabras tiene establecido el estilo de tachado.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="dc1b4-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc1b4-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span><span class="sxs-lookup"><span data-stu-id="dc1b4-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="dc1b4-108">Dirección de un valor que recibe **true** si se establece el estilo de tachado de fuente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="dc1b4-109">El estilo de fuente utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="dc1b4-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-110">It cannot be changed by an application.</span></span> <span data-ttu-id="dc1b4-111">Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc1b4-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




