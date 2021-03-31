---
title: BackColor (propiedad, características heredadas del entorno de Windows)
description: BackColor (propiedad)
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800890"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="530ce-103">BackColor (propiedad, características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="530ce-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="530ce-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="530ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="530ce-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="530ce-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="530ce-106">Devuelve el color de fondo que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="530ce-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="530ce-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="530ce-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="530ce-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Balloon. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="530ce-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="530ce-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="530ce-109">Remarks</span></span>

<span data-ttu-id="530ce-110">El intervalo válido para un color RGB normal es de 0 a 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="530ce-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="530ce-111">El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, desde menos hasta el byte más significativo, determinan la cantidad de rojo, verde y azul, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="530ce-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="530ce-112">Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="530ce-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




