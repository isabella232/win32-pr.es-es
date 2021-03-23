---
title: Trabajar con Direct3D 11, Direct3D 10 y Direct2D
description: En esta sección se describen las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API 11on12 de Direct3D y las instrucciones de portabilidad de Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103753"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="3947e-103">Trabajar con Direct3D 11, Direct3D 10 y Direct2D</span><span class="sxs-lookup"><span data-stu-id="3947e-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="3947e-104">En esta sección se describen las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API 11on12 de Direct3D y las instrucciones de portabilidad de Direct3D 11 a Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3947e-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3947e-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3947e-105">In this section</span></span>



| <span data-ttu-id="3947e-106">Tema</span><span class="sxs-lookup"><span data-stu-id="3947e-106">Topic</span></span>                                                                                             | <span data-ttu-id="3947e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3947e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3947e-108">Interoperabilidad de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3947e-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="3947e-109">D3D12 se puede usar para escribir aplicaciones en componentes.</span><span class="sxs-lookup"><span data-stu-id="3947e-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3947e-110">Direct3D 11 en 12</span><span class="sxs-lookup"><span data-stu-id="3947e-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="3947e-111">D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos de D3D11 para impulsar la API de D3D12.</span><span class="sxs-lookup"><span data-stu-id="3947e-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="3947e-112">D3D11on12 permite que los componentes escritos con D3D11 (por ejemplo, texto y la interfaz de usuario de D2D) funcionen juntos con los componentes escritos como destino de la API de D3D12.</span><span class="sxs-lookup"><span data-stu-id="3947e-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="3947e-113">D3D11on12 también habilita el traslado incremental de una aplicación de D3D11 a D3D12, ya que permite que partes de la aplicación continúen orientadas a D3D11 para simplificar, mientras que otras se dirigen a D3D12 de rendimiento, a la vez que siempre tienen una representación completa y correcta.</span><span class="sxs-lookup"><span data-stu-id="3947e-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="3947e-114">D3D11On12 simplifica el uso de técnicas de interoperabilidad para compartir recursos y sincronizar el trabajo entre las dos API.</span><span class="sxs-lookup"><span data-stu-id="3947e-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="3947e-115">Portabilidad de Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3947e-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="3947e-116">En esta sección se proporcionan instrucciones sobre cómo migrar desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3947e-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3947e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3947e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3947e-118">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3947e-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





