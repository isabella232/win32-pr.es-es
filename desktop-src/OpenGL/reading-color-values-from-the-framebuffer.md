---
title: Leer valores de color de fotogramas
description: Al usar funciones que leen los valores de color de los fotogramas, tenga en cuenta las diferencias entre leer valores RGBA y valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paletas.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL en Windows, leer valores de color de framebuffers
- leer valores de color de framebuffers OpenGL
- framebuffers, valores de color de lectura OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774893"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="16837-106">Leer valores de color de fotogramas</span><span class="sxs-lookup"><span data-stu-id="16837-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="16837-107">Al usar funciones que leen los valores de color de los fotogramas, tenga en cuenta las diferencias entre leer valores RGBA y valores de índice de color en dispositivos de color verdadero y en dispositivos basados en paletas.</span><span class="sxs-lookup"><span data-stu-id="16837-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="16837-108">En un dispositivo de color verdadero:</span><span class="sxs-lookup"><span data-stu-id="16837-108">On a true-color device:</span></span>

-   <span data-ttu-id="16837-109">Los valores RGBA se limitan al canal en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16837-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="16837-110">Los valores de índice de color se almacenan como valores RGBA en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="16837-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="16837-111">Al utilizar estos valores, debe realizar una traducción inversa desde RGBA hasta el índice lógico de la paleta.</span><span class="sxs-lookup"><span data-stu-id="16837-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="16837-112">Si dos índices lógicos tienen los mismos valores RGBA, se puede devolver el índice equivocado.</span><span class="sxs-lookup"><span data-stu-id="16837-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="16837-113">En un dispositivo basado en paleta:</span><span class="sxs-lookup"><span data-stu-id="16837-113">On a palette-based device:</span></span>

-   <span data-ttu-id="16837-114">Los valores RGBA se leen de un índice en la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="16837-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="16837-115">El índice lógico se obtiene de una tabla inversa y se extraen los componentes RGBA.</span><span class="sxs-lookup"><span data-stu-id="16837-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="16837-116">Los valores de índice de color se leen de un índice en la paleta del sistema y se usa una tabla inversa para obtener el índice de la paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="16837-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




