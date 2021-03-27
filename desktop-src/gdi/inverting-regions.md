---
description: Una aplicación invierte los colores que aparecen dentro de una región mediante una llamada a la función InvertRgn.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Invertir regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997344"
---
# <a name="inverting-regions"></a><span data-ttu-id="4bda7-103">Invertir regiones</span><span class="sxs-lookup"><span data-stu-id="4bda7-103">Inverting Regions</span></span>

<span data-ttu-id="4bda7-104">Una aplicación invierte los colores que aparecen dentro de una región mediante una llamada a la función [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) .</span><span class="sxs-lookup"><span data-stu-id="4bda7-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="4bda7-105">En las pantallas monocromáticas, **InvertRgn** hace que los píxeles blancos estén en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="4bda7-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="4bda7-106">En las pantallas de color, esta inversión depende del tipo de tecnología que se usa para generar los colores de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4bda7-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



