---
description: Al establecer esta Directiva del sistema por usuario, se especifica el orden en el que el instalador busca tres tipos de orígenes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913665"
---
# <a name="searchorder"></a><span data-ttu-id="98d88-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="98d88-103">SearchOrder</span></span>

<span data-ttu-id="98d88-104">Al establecer esta [Directiva del sistema](system-policy.md) por usuario, se especifica el orden en el que el instalador busca tres tipos de orígenes.</span><span class="sxs-lookup"><span data-stu-id="98d88-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="98d88-105">Los tipos de orígenes son:</span><span class="sxs-lookup"><span data-stu-id="98d88-105">The types of sources are:</span></span>

<span data-ttu-id="98d88-106">"n": red</span><span class="sxs-lookup"><span data-stu-id="98d88-106">"n" – network</span></span>

<span data-ttu-id="98d88-107">"m": medio (CD-ROM o DVD)</span><span class="sxs-lookup"><span data-stu-id="98d88-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="98d88-108">"u": localizador uniforme de recursos (URL)</span><span class="sxs-lookup"><span data-stu-id="98d88-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="98d88-109">Por ejemplo, para buscar primero los orígenes de red, los orígenes de medios segundo y los orígenes de direcciones URL, establezca esta directiva en un valor de "NMU".</span><span class="sxs-lookup"><span data-stu-id="98d88-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="98d88-110">Para omitir la búsqueda de un tipo de origen determinado, deje la letra correspondiente del valor.</span><span class="sxs-lookup"><span data-stu-id="98d88-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="98d88-111">Si no se establece SearchOrder, el orden de búsqueda predeterminado es red, medios y dirección URL.</span><span class="sxs-lookup"><span data-stu-id="98d88-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="98d88-112">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="98d88-112">Registry Key</span></span>

<span data-ttu-id="98d88-113">**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="98d88-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="98d88-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="98d88-114">Data Type</span></span>

<span data-ttu-id="98d88-115">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="98d88-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="98d88-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98d88-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98d88-117">Resistencia de origen</span><span class="sxs-lookup"><span data-stu-id="98d88-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



