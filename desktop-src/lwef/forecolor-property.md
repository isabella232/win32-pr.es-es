---
title: Propiedad ForeColor
description: Propiedad ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903218"
---
# <a name="forecolor-property"></a><span data-ttu-id="e5114-103">Propiedad ForeColor</span><span class="sxs-lookup"><span data-stu-id="e5114-103">ForeColor Property</span></span>

<span data-ttu-id="e5114-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5114-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e5114-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="e5114-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e5114-106">Devuelve el color de primer plano que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="e5114-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="e5114-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="e5114-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e5114-108">*agente ***. Caracteres ("*** CharacterID \* *"). Balloon. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="e5114-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5114-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5114-109">Remarks</span></span>

<span data-ttu-id="e5114-110">La propiedad **ForeColor** devuelve un valor que especifica el color del texto del globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="e5114-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="e5114-111">El intervalo válido para un color RGB normal es de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="e5114-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="e5114-112">El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, desde menos hasta el byte más significativo, determinan la cantidad de rojo, verde y azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e5114-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="e5114-113">Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="e5114-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




