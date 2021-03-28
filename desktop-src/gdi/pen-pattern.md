---
description: El atributo Pattern especifica el patrón de una pluma geométrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Patrón de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544422"
---
# <a name="pen-pattern"></a><span data-ttu-id="fed5e-103">Patrón de lápiz</span><span class="sxs-lookup"><span data-stu-id="fed5e-103">Pen Pattern</span></span>

<span data-ttu-id="fed5e-104">El atributo Pattern especifica el patrón de una pluma geométrica.</span><span class="sxs-lookup"><span data-stu-id="fed5e-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="fed5e-105">En la ilustración siguiente se muestran líneas dibujadas con diferentes lápices geométricos.</span><span class="sxs-lookup"><span data-stu-id="fed5e-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="fed5e-106">Cada lápiz se creó con un atributo de patrón diferente.</span><span class="sxs-lookup"><span data-stu-id="fed5e-106">Each pen was created using a different pattern attribute.</span></span>

![Ilustración que muestra cuatro líneas, cada una con un lápiz diferente](images/cspen-02.png)

<span data-ttu-id="fed5e-108">La primera línea de la ilustración anterior se dibuja utilizando uno de los seis patrones de trama disponibles; para obtener más información sobre los patrones de trama, vea [sombreado de lápiz](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="fed5e-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="fed5e-109">La línea siguiente se dibuja con el patrón hueco, idéntico al patrón null.</span><span class="sxs-lookup"><span data-stu-id="fed5e-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="fed5e-110">La tercera línea se dibuja mediante un patrón personalizado creado a partir de un mapa de bits de 8 por 8 píxeles.</span><span class="sxs-lookup"><span data-stu-id="fed5e-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="fed5e-111">(Para obtener más información sobre los mapas de bits y su creación, vea [mapas de bits](bitmaps.md)). La última línea se dibuja con un patrón sólido.</span><span class="sxs-lookup"><span data-stu-id="fed5e-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="fed5e-112">Al crear un pincel y pasar su identificador a la función [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) , se crea un modelo.</span><span class="sxs-lookup"><span data-stu-id="fed5e-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



