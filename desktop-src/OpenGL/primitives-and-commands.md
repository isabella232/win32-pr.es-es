---
title: Primitivas y comandos
description: Primitivas y comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitivos
- OpenGL, comandos
- primitivas OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774995"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="8be72-107">Primitivas y comandos</span><span class="sxs-lookup"><span data-stu-id="8be72-107">Primitives and Commands</span></span>

<span data-ttu-id="8be72-108">OpenGL dibuja puntos *primitivos* , segmentos de línea o polygonssubject en varios modos seleccionables.</span><span class="sxs-lookup"><span data-stu-id="8be72-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="8be72-109">Puede controlar los modos de forma independiente entre sí.</span><span class="sxs-lookup"><span data-stu-id="8be72-109">You can control modes independently of one another.</span></span> <span data-ttu-id="8be72-110">Es decir, el establecimiento de un modo no afecta a si se establecen otros modos (aunque muchos modos pueden interactuar para determinar lo que acaba finalmente en el fotogramas).</span><span class="sxs-lookup"><span data-stu-id="8be72-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="8be72-111">Para especificar primitivos, modos set y realizar otras operaciones de OpenGL, se emiten comandos en forma de llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="8be72-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="8be72-112">Los primitivos se definen mediante un grupo de uno o más *vértices*.</span><span class="sxs-lookup"><span data-stu-id="8be72-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="8be72-113">Un vértice define un punto, un punto de conexión de una línea o una esquina de un polígono con dos bordes.</span><span class="sxs-lookup"><span data-stu-id="8be72-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="8be72-114">Los datos (que se componen de coordenadas de vértices, colores, normales, coordenadas de textura y marcas de borde) se asocian con un vértice, y cada vértice y sus datos asociados se procesan de forma independiente, en orden y de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="8be72-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="8be72-115">Las únicas excepciones a esta regla son los casos en los que el grupo de vértices se debe recortar para que una primitiva determinada quepa en una región especificada.</span><span class="sxs-lookup"><span data-stu-id="8be72-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="8be72-116">En este caso, se pueden modificar los datos de vértice y crear nuevos vértices.</span><span class="sxs-lookup"><span data-stu-id="8be72-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="8be72-117">El tipo de recorte depende de la primitiva que representa el grupo de vértices.</span><span class="sxs-lookup"><span data-stu-id="8be72-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="8be72-118">Los comandos siempre se procesan en el orden en que se reciben, aunque puede haber un retraso indeterminado antes de que un comando surta efecto.</span><span class="sxs-lookup"><span data-stu-id="8be72-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="8be72-119">Esto significa que cada primitivo se dibuja completamente antes de que cualquier comando subsiguiente surta efecto.</span><span class="sxs-lookup"><span data-stu-id="8be72-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="8be72-120">También significa que los comandos de consulta de estado devuelven datos coherentes con la ejecución completa de todos los comandos OpenGL emitidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8be72-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




