---
description: En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabajar con controladores anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422794"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="1d2d1-103">Trabajar con controladores anteriores (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="1d2d1-104">En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="1d2d1-105">Cuando se trabaja con un dispositivo HAL de T&L, se calcula la intensidad de la niebla pero no se aplica la operación de valor absoluto a este valor.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="1d2d1-106">En su lugar, el valor se deja negativo si es lo que se calcula.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="1d2d1-107">La mejor manera de evitar esta situación es configurar las transformaciones adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="1d2d1-108">Un método menos preferido es hacer que los valores de la niebla-Start y de la niebla-end sean negativos.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="1d2d1-109">Para buscar un controlador de Direct3D 9, busque un valor distinto de cero para D3DDEVCAPS2 \_ STREAMOFFSET en el miembro DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="1d2d1-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d2d1-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d2d1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d2d1-111">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="1d2d1-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



