---
description: La clave del registro EUDCCodeRange define los intervalos de código del carácter definido por el usuario final (EUDC) para varias páginas de códigos (juegos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688339"
---
# <a name="eudccoderange"></a><span data-ttu-id="f4cf7-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="f4cf7-103">EUDCCodeRange</span></span>

<span data-ttu-id="f4cf7-104">La clave del registro EUDCCodeRange define los intervalos de código del [carácter definido por el usuario final (EUDC)](end-user-defined-characters.md) para varias páginas de códigos (juegos de caracteres).</span><span class="sxs-lookup"><span data-stu-id="f4cf7-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="f4cf7-105">Solo se usa en las herramientas que crean EUDCs y no es de interés directo para los usuarios de EUDC.</span><span class="sxs-lookup"><span data-stu-id="f4cf7-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="f4cf7-106">Esta clave del registro tiene la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="f4cf7-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="f4cf7-107">HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="f4cf7-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="f4cf7-108">El formato es:</span><span class="sxs-lookup"><span data-stu-id="f4cf7-108">The format is:</span></span>

<span data-ttu-id="f4cf7-109">EUDCCodeRange CodePage = Fromto \[ , fromto\]</span><span class="sxs-lookup"><span data-stu-id="f4cf7-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="f4cf7-110">donde:</span><span class="sxs-lookup"><span data-stu-id="f4cf7-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cf7-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="f4cf7-111">CodePage</span></span> | <span data-ttu-id="f4cf7-112">Una de las cadenas "932" (japonés), "936" (Chino Simplificado), "949" (Coreano), "950" (chino tradicional) o "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="f4cf7-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="f4cf7-113">No se admiten otros valores.</span><span class="sxs-lookup"><span data-stu-id="f4cf7-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="f4cf7-114">Fromto</span><span class="sxs-lookup"><span data-stu-id="f4cf7-114">FromTo</span></span>   | <span data-ttu-id="f4cf7-115">Valor de cadena que consta de un par de valores hexadecimales de 4 dígitos separados por un guión (-).</span><span class="sxs-lookup"><span data-stu-id="f4cf7-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="f4cf7-116">Se pueden especificar hasta cuatro valores de a, pero cada uno debe estar separado del valor anterior por una coma (,).</span><span class="sxs-lookup"><span data-stu-id="f4cf7-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="f4cf7-117">A continuación se muestran los valores correctos para la entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="f4cf7-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="f4cf7-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4cf7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4cf7-119">Entradas del registro de EUDC</span><span class="sxs-lookup"><span data-stu-id="f4cf7-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="f4cf7-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="f4cf7-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



