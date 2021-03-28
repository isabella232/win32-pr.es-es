---
description: La función ExcludeUpdateRgn excluye la región de actualización de la región de recorte para el contexto de dispositivo de pantalla.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusión de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082360"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="02be5-103">Exclusión de la región de actualización</span><span class="sxs-lookup"><span data-stu-id="02be5-103">Excluding the Update Region</span></span>

<span data-ttu-id="02be5-104">La función [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) excluye la región de actualización de la región de recorte para el contexto de dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="02be5-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="02be5-105">Esta función es útil cuando se dibuja en una ventana distinta de cuando \_ se procesa un mensaje de pintura de WM.</span><span class="sxs-lookup"><span data-stu-id="02be5-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="02be5-106">Impide dibujar en las áreas que se van a actualizar durante el siguiente mensaje de pintura de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="02be5-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



