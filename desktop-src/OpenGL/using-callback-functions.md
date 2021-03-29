---
title: Usar funciones de devolución de llamada
description: Las funciones de devolución de llamada GLU, gluBeginPolygon, gluTessVertex, gluNextContour y gluEndPolygon, son similares a las funciones de polígono de OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilidad OpenGL (GLU), funciones de devolución de llamada
- GLU (utilidad OpenGL), funciones de devolución de llamada
- Utilidad OpenGL (GLU), Teselación
- GLU (utilidad OpenGL), Teselación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903311"
---
# <a name="using-callback-functions"></a><span data-ttu-id="f4c52-107">Usar funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="f4c52-107">Using Callback Functions</span></span>

<span data-ttu-id="f4c52-108">Las funciones de devolución de llamada GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)y [**gluEndPolygon**](gluendpolygon.md), son similares a las funciones de polígono de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f4c52-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="f4c52-109">Normalmente guardan los datos de los triángulos, las mallas de triángulo y los ventiladores de triángulo en las estructuras de datos definidas por el usuario o en las listas de visualización de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f4c52-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="f4c52-110">Para representar los polígonos, otro código atraviesa las estructuras de datos o llama a las listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="f4c52-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="f4c52-111">Aunque las funciones de devolución de llamada podrían llamar a funciones de OpenGL para mostrar polígonos directamente, normalmente no se hace esto, ya que la teselación puede consumir muchos recursos computacionalmente.</span><span class="sxs-lookup"><span data-stu-id="f4c52-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="f4c52-112">Se recomienda guardar los datos si hay alguna posibilidad de que desee volver a mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="f4c52-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="f4c52-113">Se garantiza que las funciones de teselación GLU nunca devuelven los vértices nuevos, por lo que nunca se necesita la interpolación de vértices, coordenadas de textura o colores.</span><span class="sxs-lookup"><span data-stu-id="f4c52-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 




