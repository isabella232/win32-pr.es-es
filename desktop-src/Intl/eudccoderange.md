---
description: La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final (EUDC) para varias páginas de códigos (juegos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120680"
---
# <a name="eudccoderange"></a><span data-ttu-id="99a2a-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="99a2a-103">EUDCCodeRange</span></span>

<span data-ttu-id="99a2a-104">La clave del Registro EUDCCodeRange define intervalos de código de caracteres definidos por el usuario final [(EUDC)](end-user-defined-characters.md) para varias páginas de códigos (juegos de caracteres).</span><span class="sxs-lookup"><span data-stu-id="99a2a-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="99a2a-105">Solo lo usan herramientas que crean EUDC y no es un problema directo para los usuarios de EUDC.</span><span class="sxs-lookup"><span data-stu-id="99a2a-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="99a2a-106">Esta clave del Registro tiene la siguiente ubicación del Registro:</span><span class="sxs-lookup"><span data-stu-id="99a2a-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="99a2a-107">HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="99a2a-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="99a2a-108">El formato es:</span><span class="sxs-lookup"><span data-stu-id="99a2a-108">The format is:</span></span>

<span data-ttu-id="99a2a-109">EUDCCodeRange CodePage=FromTo \[ ,FromTo\]</span><span class="sxs-lookup"><span data-stu-id="99a2a-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="99a2a-110">donde:</span><span class="sxs-lookup"><span data-stu-id="99a2a-110">where:</span></span>



| <span data-ttu-id="99a2a-111">Value</span><span class="sxs-lookup"><span data-stu-id="99a2a-111">Value</span></span>         | <span data-ttu-id="99a2a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="99a2a-112">Description</span></span>                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a2a-113">CodePage</span><span class="sxs-lookup"><span data-stu-id="99a2a-113">CodePage</span></span> | <span data-ttu-id="99a2a-114">Una de las cadenas "932" (japonés), "936" (chino simplificado), "949" (coreano), "950" (chino tradicional) o "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="99a2a-114">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="99a2a-115">No se admite ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="99a2a-115">No other values are supported.</span></span>                                     |
| <span data-ttu-id="99a2a-116">FromTo</span><span class="sxs-lookup"><span data-stu-id="99a2a-116">FromTo</span></span>   | <span data-ttu-id="99a2a-117">Valor de cadena que consta de un par de valores hexadecimales de 4 dígitos separados por un guion (-).</span><span class="sxs-lookup"><span data-stu-id="99a2a-117">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="99a2a-118">Se pueden especificar hasta cuatro valores FromTo, pero cada uno debe estar separado del valor anterior por una coma (,).</span><span class="sxs-lookup"><span data-stu-id="99a2a-118">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="99a2a-119">Estos son los valores correctos para la entrada del Registro.</span><span class="sxs-lookup"><span data-stu-id="99a2a-119">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="99a2a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99a2a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a2a-121">Entradas del Registro eudc</span><span class="sxs-lookup"><span data-stu-id="99a2a-121">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="99a2a-122">EUDC</span><span class="sxs-lookup"><span data-stu-id="99a2a-122">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



