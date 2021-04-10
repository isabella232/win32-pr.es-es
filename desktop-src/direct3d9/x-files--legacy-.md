---
description: El formato de archivo X hace referencia a los archivos con la extensión de nombre de archivo. x.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: Archivos X (heredado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906433"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="a5fc5-103">Archivos X (heredado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="a5fc5-104">El formato de archivo X hace referencia a los archivos con la extensión de nombre de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="a5fc5-105">Los archivos X se introdujeron con DirectX 2,0.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="a5fc5-106">Posteriormente, se lanzó una versión binaria de este formato con DirectX 3,0, que también se describe en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="a5fc5-107">DirectX 6,0 presentó interfaces y métodos que permiten leer y escribir en archivos. x.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="a5fc5-108">Los archivos X proporcionan un formato controlado por plantillas que permite el almacenamiento de mallas, texturas, animaciones y objetos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="a5fc5-109">La compatibilidad con conjuntos de animaciones le permite almacenar rutas de acceso predefinidas para la reproducción en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="a5fc5-110">También se admiten la creación de instancias y jerarquías.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="a5fc5-111">La creación de instancias habilita varias referencias a un objeto, como una malla, mientras que almacena sus datos solo una vez por cada archivo.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="a5fc5-112">Las jerarquías se utilizan para expresar las relaciones entre los registros de datos.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="a5fc5-113">El formato de archivo. x proporciona primitivas de datos de bajo nivel en las que las aplicaciones definen primitivos de nivel superior a través de plantillas.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="a5fc5-114">Los modelos tridimensionales creados en aplicaciones Maya de 3ds Max o de alias Wavefront de discretas \| se pueden convertir en archivos. x con las extensiones de DirectX para el alias Maya.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="a5fc5-115">En esta sección se describe la estructura de los archivos. x y cómo usarlos en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="a5fc5-116">La información se divide en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a5fc5-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="a5fc5-117">Cargar un archivo X (heredado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="a5fc5-118">Guardar en un archivo X (heredado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="a5fc5-119">Definir un cubo simple (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="a5fc5-120">Agregar texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="a5fc5-121">Agregar Marcos y animaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5fc5-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="a5fc5-122">Para obtener más información sobre el formato de archivo. x, consulte [x File Reference](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc5-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="a5fc5-123">Para obtener más información sobre la API de archivos. x, consulte [referencia de archivo x (heredado)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="a5fc5-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5fc5-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5fc5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5fc5-125">Introducción</span><span class="sxs-lookup"><span data-stu-id="a5fc5-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



