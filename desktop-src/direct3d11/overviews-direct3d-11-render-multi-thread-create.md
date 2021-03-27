---
title: Creación de objetos con multithreading
description: Use la interfaz ID3D11Device para crear recursos y objetos, use ID3D11DeviceContext para la representación.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994251"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="fcdcc-103">Creación de objetos con multithreading</span><span class="sxs-lookup"><span data-stu-id="fcdcc-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="fcdcc-104">Use la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para la [representación](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="fcdcc-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="fcdcc-105">Estos son algunos ejemplos de cómo crear recursos:</span><span class="sxs-lookup"><span data-stu-id="fcdcc-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="fcdcc-106">Cómo: crear un búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="fcdcc-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="fcdcc-107">Cómo: crear un búfer de índice</span><span class="sxs-lookup"><span data-stu-id="fcdcc-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="fcdcc-108">Cómo: crear un búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="fcdcc-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="fcdcc-109">Cómo: inicializar una textura desde un archivo</span><span class="sxs-lookup"><span data-stu-id="fcdcc-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="fcdcc-110">Consideraciones sobre multithreading</span><span class="sxs-lookup"><span data-stu-id="fcdcc-110">Multithreading Considerations</span></span>

<span data-ttu-id="fcdcc-111">La cantidad de simultaneidad de la creación y representación de recursos que puede alcanzar la aplicación depende del nivel de compatibilidad con multithreading que implementa el controlador.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="fcdcc-112">Si el controlador admite las operaciones de creación simultáneas, la aplicación debe tener muchos menos problemas de simultaneidad.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="fcdcc-113">Sin embargo, si el controlador no admite la creación de objetos simultáneos, la cantidad de simultaneidad es muy limitada.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="fcdcc-114">Para comprender la cantidad de soporte técnico disponible en un controlador, consulte en el controlador el valor del miembro **DriverConcurrentCreates** de la estructura de [**\_ \_ \_ subprocesos de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) .</span><span class="sxs-lookup"><span data-stu-id="fcdcc-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="fcdcc-115">Para obtener más información acerca de cómo comprobar la compatibilidad de los controladores con multithreading, consulte [Cómo: comprobar la compatibilidad](overviews-direct3d-11-render-multi-thread-support.md)de los controladores.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="fcdcc-116">Las operaciones simultáneas no implican necesariamente un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="fcdcc-117">Por ejemplo, la creación y carga de una textura suele estar limitada por el ancho de banda de memoria.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="fcdcc-118">Es posible que el intento de crear y cargar varias texturas no sea más rápido que la realización de una textura a la vez, incluso si esto deja inactivas varios núcleos de CPU.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="fcdcc-119">Sin embargo, la creación de varios sombreadores con varios subprocesos puede aumentar el rendimiento, ya que esta operación es menos dependiente de los recursos del sistema, como el ancho de banda de memoria.</span><span class="sxs-lookup"><span data-stu-id="fcdcc-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="fcdcc-120">Cuando el controlador y el hardware de gráficos admiten el multithreading, normalmente se pueden inicializar de forma más eficaz los recursos recién creados pasando un puntero a los datos iniciales en el parámetro *pInitialData* (por ejemplo, en una llamada al método [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).</span><span class="sxs-lookup"><span data-stu-id="fcdcc-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcdcc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcdcc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcdcc-122">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="fcdcc-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




