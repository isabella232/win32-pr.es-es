---
description: Un pincel sólido es un pincel lógico que contiene 64 píxeles del mismo color.
ms.assetid: 920014c7-d1ef-4b98-8c92-c4169be52cb9
title: Pincel sólido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7cd7a2140ece4bf93ac6f8525be461b70e28fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985378"
---
# <a name="solid-brush"></a><span data-ttu-id="77fb2-103">Pincel sólido</span><span class="sxs-lookup"><span data-stu-id="77fb2-103">Solid Brush</span></span>

<span data-ttu-id="77fb2-104">Un *pincel sólido* es un pincel lógico que contiene 64 píxeles del mismo color.</span><span class="sxs-lookup"><span data-stu-id="77fb2-104">A *solid brush* is a logical brush that contains 64 pixels of the same color.</span></span> <span data-ttu-id="77fb2-105">Una aplicación puede crear un pincel lógico sólido mediante una llamada a la función [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) , que especifica el color del pincel necesario.</span><span class="sxs-lookup"><span data-stu-id="77fb2-105">An application can create a solid logical brush by calling the [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) function, specifying the color of the brush required.</span></span> <span data-ttu-id="77fb2-106">Después de crear el pincel sólido, la aplicación puede seleccionarlo en su contexto de dispositivo y usarlo para pintar formas rellenas.</span><span class="sxs-lookup"><span data-stu-id="77fb2-106">After creating the solid brush, the application can select it into its device context and use it to paint filled shapes.</span></span>

 

 



