---
description: Una aplicación debe usar una estructura RECT para definir un rectángulo.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordenadas del rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997317"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="bfced-103">Coordenadas del rectángulo</span><span class="sxs-lookup"><span data-stu-id="bfced-103">Rectangle Coordinates</span></span>

<span data-ttu-id="bfced-104">Una aplicación debe usar una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para definir un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="bfced-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="bfced-105">La estructura especifica las coordenadas de dos puntos: las esquinas superior izquierda e inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="bfced-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="bfced-106">Los lados del rectángulo se extienden desde estos dos puntos y son paralelos a los ejes x e y.</span><span class="sxs-lookup"><span data-stu-id="bfced-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="bfced-107">Los valores de las coordenadas de un rectángulo se expresan como enteros con signo.</span><span class="sxs-lookup"><span data-stu-id="bfced-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="bfced-108">El valor de la coordenada del lado derecho de un rectángulo debe ser mayor que el del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="bfced-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="bfced-109">Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="bfced-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="bfced-110">Dado que las aplicaciones pueden usar rectángulos para muchos fines diferentes, las funciones de rectángulo no usan una unidad de medida explícita.</span><span class="sxs-lookup"><span data-stu-id="bfced-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="bfced-111">En su lugar, todas las coordenadas y dimensiones del rectángulo se proporcionan en valores lógicos con signo.</span><span class="sxs-lookup"><span data-stu-id="bfced-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="bfced-112">El modo de asignación y la función en la que se utiliza el rectángulo determinan las unidades de medida.</span><span class="sxs-lookup"><span data-stu-id="bfced-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="bfced-113">Para obtener más información sobre las coordenadas y los modos de asignación, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="bfced-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
