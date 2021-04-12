---
description: El tipo de datos Language es una cadena de texto que contiene uno o más identificadores de idioma numéricos válidos. Si hay dos o más identificadores de idioma, deben separarse con comas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275436"
---
# <a name="language"></a><span data-ttu-id="bea15-104">Idioma</span><span class="sxs-lookup"><span data-stu-id="bea15-104">Language</span></span>

<span data-ttu-id="bea15-105">El tipo de datos Language es una cadena de texto que contiene uno o más identificadores de idioma numéricos válidos.</span><span class="sxs-lookup"><span data-stu-id="bea15-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="bea15-106">Si hay dos o más identificadores de idioma, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="bea15-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="bea15-107">El tipo de datos Language es un valor de 16 bits que es la combinación de los identificadores numéricos principales y de subidioma.</span><span class="sxs-lookup"><span data-stu-id="bea15-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="bea15-108">El LANGID principal comprende los bits del 0 al 9, mientras que el identificador de subidioma es de bits 10 a 15.</span><span class="sxs-lookup"><span data-stu-id="bea15-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="bea15-109">Para obtener una lista de los identificadores numéricos principales y secundarios, vea el tema sobre las [constantes y las cadenas de identificador de idioma](../intl/language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="bea15-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="bea15-110">En el caso de los identificadores de idioma principal, el intervalo 0x200 a 0x3ff es definible por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bea15-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="bea15-111">El intervalo 0x000 a 0x1ff está reservado para el uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="bea15-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="bea15-112">En el caso de los identificadores de subidioma, el intervalo de 0x20 a 0x3F es definible por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bea15-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="bea15-113">El intervalo de 0x00 a 0x1F está reservado para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="bea15-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
