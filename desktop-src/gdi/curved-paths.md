---
description: Trazados curvos
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Trazados curvos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908503"
---
# <a name="curved-paths"></a><span data-ttu-id="d3fd8-103">Trazados curvos</span><span class="sxs-lookup"><span data-stu-id="d3fd8-103">Curved Paths</span></span>

<span data-ttu-id="d3fd8-104">Una aplicación puede acoplar las curvas en un trazado mediante una llamada a la función [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) .</span><span class="sxs-lookup"><span data-stu-id="d3fd8-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="d3fd8-105">Esta función es especialmente útil para las aplicaciones que se ajustan al texto en el contorno de una ruta de acceso que contiene curvas.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="d3fd8-106">Para ajustar el texto, la aplicación debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="d3fd8-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="d3fd8-107">Cree la ruta de acceso donde aparece el texto.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="d3fd8-108">Llame a la función [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para convertir las curvas de un trazado en segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="d3fd8-109">Llame a la función [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esos segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="d3fd8-110">Calcular la longitud de cada línea y el ancho de cada carácter de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="d3fd8-111">Use datos de ancho de línea y de ancho de caracteres para colocar cada carácter a lo largo de la curva.</span><span class="sxs-lookup"><span data-stu-id="d3fd8-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



