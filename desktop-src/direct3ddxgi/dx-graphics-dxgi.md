---
description: DXGI
ms.assetid: 9565e874-5a8d-4b4b-a2a4-391e46922cc1
title: DXGI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e100d068d12f651c2602b29af75181607a038
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343500"
---
# <a name="dxgi"></a><span data-ttu-id="503a0-103">DXGI</span><span class="sxs-lookup"><span data-stu-id="503a0-103">DXGI</span></span>

<span data-ttu-id="503a0-104">Microsoft Infraestructura de gráficos de DirectX (DXGI) controla la enumeración de adaptadores gráficos, la enumeración de modos de presentación, la selección de formatos de búfer, el uso compartido de recursos entre procesos (por ejemplo, entre aplicaciones y Administrador de ventanas de escritorio (DWM)) y la presentación de fotogramas representados en una ventana o monitor para su presentación.</span><span class="sxs-lookup"><span data-stu-id="503a0-104">Microsoft DirectX Graphics Infrastructure (DXGI) handles enumerating graphics adapters, enumerating display modes, selecting buffer formats, sharing resources between processes (such as, between applications and the Desktop Window Manager (DWM)), and presenting rendered frames to a window or monitor for display.</span></span>

<span data-ttu-id="503a0-105">Direct3D 10, Direct3D 11 y Direct3D 12 usan DXGI.</span><span class="sxs-lookup"><span data-stu-id="503a0-105">DXGI is used by Direct3D 10, Direct3D 11 and Direct3D 12.</span></span>

<span data-ttu-id="503a0-106">Aunque la mayoría de la programación de gráficos se realiza mediante Direct3D, puede usar DXGI para presentar fotogramas en una ventana, un monitor u otro componente gráfico para la composición y la presentación finales.</span><span class="sxs-lookup"><span data-stu-id="503a0-106">Though most graphics programming is done using Direct3D, you can use DXGI to present frames to a window, monitor, or other graphics component for eventual composition and display.</span></span> <span data-ttu-id="503a0-107">También puede usar DXGI para leer el contenido de un monitor.</span><span class="sxs-lookup"><span data-stu-id="503a0-107">You can also use DXGI to read the contents on a monitor.</span></span>

<span data-ttu-id="503a0-108">Este conjunto de documentación contiene información sobre la programación con DXGI.</span><span class="sxs-lookup"><span data-stu-id="503a0-108">This documentation set contains information about programming with DXGI.</span></span>



| <span data-ttu-id="503a0-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="503a0-109">Requirement</span></span>                                  | <span data-ttu-id="503a0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="503a0-110">Value</span></span>                                                                                               |
|-----------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503a0-111">Entornos de tiempo de ejecución compatibles</span><span class="sxs-lookup"><span data-stu-id="503a0-111">Supported runtime environments</span></span>    | <dl> <span data-ttu-id="503a0-112"><dt>Windows/C++</dt></span><span class="sxs-lookup"><span data-stu-id="503a0-112"><dt>Windows/C++</dt></span></span> </dl>         |
| <span data-ttu-id="503a0-113">Idiomas de programación recomendados</span><span class="sxs-lookup"><span data-stu-id="503a0-113">Recommended programming languages</span></span> | <span data-ttu-id="503a0-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="503a0-114">C/C++</span></span>                                                                                          |
| <span data-ttu-id="503a0-115">Cliente mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="503a0-115">Minimum supported Client</span></span>          | <dl> <span data-ttu-id="503a0-116"><dt>Windows Vista</dt></span><span class="sxs-lookup"><span data-stu-id="503a0-116"><dt>Windows Vista</dt></span></span> </dl>       |
| <span data-ttu-id="503a0-117">Servidor mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="503a0-117">Minimum supported Server</span></span>          | <dl> <span data-ttu-id="503a0-118"><dt>Windows Server 2008</dt></span><span class="sxs-lookup"><span data-stu-id="503a0-118"><dt>Windows Server 2008</dt></span></span> </dl> |



-   [<span data-ttu-id="503a0-119">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="503a0-119">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
-   [<span data-ttu-id="503a0-120">Referencia de DXGI</span><span class="sxs-lookup"><span data-stu-id="503a0-120">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)

 

 



