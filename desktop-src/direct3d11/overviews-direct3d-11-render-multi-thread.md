---
title: MultiThreading
description: Direct3D 11 implementa la compatibilidad con la creación y representación de objetos mediante varios subprocesos.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269094"
---
# <a name="multithreading"></a><span data-ttu-id="a3e36-103">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="a3e36-103">MultiThreading</span></span>

<span data-ttu-id="a3e36-104">Direct3D 11 implementa la compatibilidad con la creación y representación de objetos mediante varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a3e36-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3e36-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a3e36-105">In this section</span></span>



| <span data-ttu-id="a3e36-106">Tema</span><span class="sxs-lookup"><span data-stu-id="a3e36-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="a3e36-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3e36-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3e36-108">Introducción a multithreading en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a3e36-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="a3e36-109">El multithreading está diseñado para mejorar el rendimiento mediante la realización de trabajos mediante uno o varios subprocesos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a3e36-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="a3e36-110">Creación de objetos con multithreading</span><span class="sxs-lookup"><span data-stu-id="a3e36-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="a3e36-111">Use la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para la [representación](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="a3e36-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="a3e36-112">Representación inmediata y diferida</span><span class="sxs-lookup"><span data-stu-id="a3e36-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="a3e36-113">Direct3D 11 admite dos tipos de representación: inmediato y aplazado.</span><span class="sxs-lookup"><span data-stu-id="a3e36-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="a3e36-114">Ambos se implementan mediante la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="a3e36-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="a3e36-115">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="a3e36-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="a3e36-116">Una lista de comandos es una secuencia de comandos de GPU que se pueden grabar y reproducir.</span><span class="sxs-lookup"><span data-stu-id="a3e36-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="a3e36-117">Una lista de comandos puede mejorar el rendimiento reduciendo la cantidad de sobrecarga generada por el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a3e36-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="a3e36-118">Diferencias de subprocesos entre versiones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a3e36-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="a3e36-119">Muchos modelos de programación multiproceso hacen uso de primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas e impedir que más de un subproceso tenga acceso a código a la vez.</span><span class="sxs-lookup"><span data-stu-id="a3e36-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="a3e36-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3e36-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3e36-121">Cómo: comprobar la compatibilidad de controladores</span><span class="sxs-lookup"><span data-stu-id="a3e36-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="a3e36-122">Representación</span><span class="sxs-lookup"><span data-stu-id="a3e36-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





