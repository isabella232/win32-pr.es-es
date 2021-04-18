---
description: Un &\# 0034; juego de caracteres&\# 0034; es una asignación de caracteres a sus valores de código de identificación.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Juegos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686722"
---
# <a name="character-sets"></a><span data-ttu-id="3d572-103">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="3d572-103">Character Sets</span></span>

<span data-ttu-id="3d572-104">Un "juego de caracteres" es una asignación de caracteres a sus valores de código de identificación.</span><span class="sxs-lookup"><span data-stu-id="3d572-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="3d572-105">El juego de caracteres que se usa con más frecuencia en los equipos de hoy en día es [Unicode](unicode.md), un estándar global para la codificación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3d572-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="3d572-106">Internamente, las aplicaciones de Windows utilizan la implementación UTF-16 de Unicode.</span><span class="sxs-lookup"><span data-stu-id="3d572-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="3d572-107">En UTF-16, la mayoría de los caracteres se identifican mediante códigos de dos bytes.</span><span class="sxs-lookup"><span data-stu-id="3d572-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="3d572-108">Los caracteres complementarios usados con menos frecuencia se representan mediante un par suplente, que es un par de códigos de dos bytes.</span><span class="sxs-lookup"><span data-stu-id="3d572-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="3d572-109">Para obtener más información, vea [suplentes y caracteres adicionales](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="3d572-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="3d572-110">Algunas aplicaciones de Windows deben funcionar con los juegos de caracteres más antiguos que son nativos de Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="3d572-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="3d572-111">[Las páginas de códigos de Windows](code-pages.md) permiten que la aplicación funcione con estos juegos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3d572-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="3d572-112">Estos juegos de caracteres se pueden dividir en:</span><span class="sxs-lookup"><span data-stu-id="3d572-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="3d572-113">[Juegos de caracteres de un solo byte](single-byte-character-sets.md) (SBCS).</span><span class="sxs-lookup"><span data-stu-id="3d572-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="3d572-114">En un SBCS, cada carácter se identifica con un valor de ancho de un byte.</span><span class="sxs-lookup"><span data-stu-id="3d572-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="3d572-115">Juegos de caracteres multibyte, en particular, los [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS).</span><span class="sxs-lookup"><span data-stu-id="3d572-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="3d572-116">Los juegos de caracteres multibyte proporcionan un medio para representar el gran número de caracteres en muchos idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="3d572-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="3d572-117">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="3d572-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3d572-118">Páginas de códigos</span><span class="sxs-lookup"><span data-stu-id="3d572-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="3d572-119">Juegos de caracteres de doble byte</span><span class="sxs-lookup"><span data-stu-id="3d572-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="3d572-120">Juegos de caracteres de un solo byte</span><span class="sxs-lookup"><span data-stu-id="3d572-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="3d572-121">Suplentes y caracteres suplementarios</span><span class="sxs-lookup"><span data-stu-id="3d572-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="3d572-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="3d572-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="3d572-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d572-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d572-124">Acerca de los juegos de caracteres y Unicode</span><span class="sxs-lookup"><span data-stu-id="3d572-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



