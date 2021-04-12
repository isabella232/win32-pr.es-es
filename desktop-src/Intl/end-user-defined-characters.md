---
description: Los caracteres definidos por el usuario final (EUDC) en los juegos de caracteres de doble byte (DBCS) y los caracteres de área de uso privado (PUA) de Unicode son caracteres personalizados.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caracteres de área de uso privado y definidos por el usuario final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361227"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="6f410-103">Caracteres de área de uso privado y definidos por el usuario final</span><span class="sxs-lookup"><span data-stu-id="6f410-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="6f410-104">Los caracteres definidos por el usuario final (EUDC) en los [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) y los caracteres de área de uso privado (PUA) de [Unicode](unicode.md) son caracteres personalizados.</span><span class="sxs-lookup"><span data-stu-id="6f410-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="6f410-105">Pueden definirse e implementarse a través de un usuario final o de otra entidad, como un fabricante de equipo, un grupo de usuarios, un organismo gubernamental o una empresa de diseño de fuentes.</span><span class="sxs-lookup"><span data-stu-id="6f410-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="6f410-106">Su uso permite a los usuarios formar nombres y otras palabras mediante caracteres que no están disponibles en las fuentes de pantalla y impresora estándar.</span><span class="sxs-lookup"><span data-stu-id="6f410-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="6f410-107">Los caracteres EUDC y PUA se pueden asignar de forma diferente o no asignarse en absoluto en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6f410-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="6f410-108">Algunas páginas de códigos tienen extensiones que reutilizan el intervalo de EUDC y estas extensiones pueden entrar en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="6f410-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="6f410-109">En otros casos, un fabricante podría proporcionar un conjunto personalizado de caracteres en uno de estos intervalos.</span><span class="sxs-lookup"><span data-stu-id="6f410-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="6f410-110">Además, los grupos de usuarios pueden intentar proporcionar caracteres adicionales en PUA.</span><span class="sxs-lookup"><span data-stu-id="6f410-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="6f410-111">Diferentes combinaciones de estos casos pueden causar conflictos.</span><span class="sxs-lookup"><span data-stu-id="6f410-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="6f410-112">Al crear aplicaciones que se basan en caracteres EUDC o PUA, debe tener en cuenta las interpretaciones conflictivas de un punto de código individual.</span><span class="sxs-lookup"><span data-stu-id="6f410-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="6f410-113">En los temas siguientes se describen las fuentes que admiten EUDCs y el acceso y la administración de estos caracteres:</span><span class="sxs-lookup"><span data-stu-id="6f410-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="6f410-114">Juegos de caracteres y fuentes</span><span class="sxs-lookup"><span data-stu-id="6f410-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="6f410-115">Entradas del registro de EUDC</span><span class="sxs-lookup"><span data-stu-id="6f410-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="6f410-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f410-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f410-117">Acerca de los juegos de caracteres y Unicode</span><span class="sxs-lookup"><span data-stu-id="6f410-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



