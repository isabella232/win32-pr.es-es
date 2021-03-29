---
title: BorderColor (propiedad)
description: BorderColor (propiedad)
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486766"
---
# <a name="bordercolor-property"></a><span data-ttu-id="a30f1-103">BorderColor (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a30f1-103">BorderColor Property</span></span>

<span data-ttu-id="a30f1-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a30f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a30f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a30f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a30f1-106">Devuelve el color del borde que se muestra actualmente para la ventana de globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="a30f1-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a30f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a30f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a30f1-108">\* agente ***. Caracteres ("*** CharacterID \***").** Balloon. BorderColor</span><span class="sxs-lookup"><span data-stu-id="a30f1-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a30f1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a30f1-109">Remarks</span></span>

<span data-ttu-id="a30f1-110">El intervalo válido para un color RGB normal es de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="a30f1-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="a30f1-111">El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, desde menos hasta el byte más significativo, determinan la cantidad de rojo, verde y azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a30f1-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="a30f1-112">Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="a30f1-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




