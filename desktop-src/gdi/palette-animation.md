---
description: La animación de paleta es una técnica para simular el movimiento mediante el cambio rápido de los colores de las entradas seleccionadas en una paleta de colores.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animación de paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811905"
---
# <a name="palette-animation"></a><span data-ttu-id="a01e1-103">Animación de paleta</span><span class="sxs-lookup"><span data-stu-id="a01e1-103">Palette Animation</span></span>

<span data-ttu-id="a01e1-104">La animación de paleta es una técnica para simular el movimiento mediante el cambio rápido de los colores de las entradas seleccionadas en una paleta de colores.</span><span class="sxs-lookup"><span data-stu-id="a01e1-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="a01e1-105">Una aplicación puede llevar a cabo la animación de la paleta mediante la creación de una paleta lógica que contiene entradas "reservadas" y, a continuación, el uso de la función [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar los colores de esas entradas reservadas.</span><span class="sxs-lookup"><span data-stu-id="a01e1-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="a01e1-106">Una aplicación crea una entrada reservada en una paleta lógica estableciendo el miembro **peFlags** de la estructura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) en la \_ marca reservada de PC.</span><span class="sxs-lookup"><span data-stu-id="a01e1-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="a01e1-107">Una vez seleccionada y realizada esta paleta lógica, la aplicación puede llamar a la función [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para cambiar una o varias entradas reservadas.</span><span class="sxs-lookup"><span data-stu-id="a01e1-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="a01e1-108">Si la paleta determinada está asociada a la ventana activa, el sistema actualiza los colores de la pantalla inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a01e1-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
