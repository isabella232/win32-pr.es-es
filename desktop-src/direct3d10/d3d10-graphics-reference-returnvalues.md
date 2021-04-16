---
description: La tabla siguiente contiene los códigos de retorno de las funciones de la API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Códigos de retorno de Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686434"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="1677a-103">Códigos de retorno de Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="1677a-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="1677a-104">La tabla siguiente contiene los códigos de retorno de las funciones de la API.</span><span class="sxs-lookup"><span data-stu-id="1677a-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="1677a-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1677a-105">HRESULT</span></span>                                         | <span data-ttu-id="1677a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1677a-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1677a-107">\_ \_ \_ No \_ se encontró el archivo de error D3D10</span><span class="sxs-lookup"><span data-stu-id="1677a-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="1677a-108">No se encontró el archivo.</span><span class="sxs-lookup"><span data-stu-id="1677a-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="1677a-109">ERROR de D3D10 \_ \_ demasiados \_ \_ \_ objetos de estado único \_</span><span class="sxs-lookup"><span data-stu-id="1677a-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="1677a-110">Hay demasiadas instancias únicas de un tipo determinado de [objeto de estado](d3d10-graphics-programming-guide-api-features-state-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1677a-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="1677a-111">D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="1677a-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="1677a-112">La llamada al método no es válida.</span><span class="sxs-lookup"><span data-stu-id="1677a-112">The method call is invalid.</span></span> <span data-ttu-id="1677a-113">Por ejemplo, el parámetro de un método no puede ser un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="1677a-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="1677a-114">D3DERR \_ WASSTILLDRAWING</span><span class="sxs-lookup"><span data-stu-id="1677a-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="1677a-115">La operación de blit anterior que está transfiriendo información a o desde esta superficie está incompleta.</span><span class="sxs-lookup"><span data-stu-id="1677a-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="1677a-116">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="1677a-116">E\_FAIL</span></span>                                         | <span data-ttu-id="1677a-117">Se intentó crear un dispositivo con la [capa de depuración](d3d10-graphics-programming-guide-api-features-layers.md) habilitada y la capa no está instalada.</span><span class="sxs-lookup"><span data-stu-id="1677a-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="1677a-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1677a-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="1677a-119">Se pasó un parámetro no válido a la función que devuelve.</span><span class="sxs-lookup"><span data-stu-id="1677a-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="1677a-120">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1677a-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="1677a-121">Direct3D no pudo asignar memoria suficiente para completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="1677a-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="1677a-122">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="1677a-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="1677a-123">La llamada al método no se implementa con la combinación de parámetros pasada.</span><span class="sxs-lookup"><span data-stu-id="1677a-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="1677a-124">S \_ false</span><span class="sxs-lookup"><span data-stu-id="1677a-124">S\_FALSE</span></span>                                        | <span data-ttu-id="1677a-125">Valor de éxito alternativo, que indica una finalización correcta pero no estándar (el significado exacto depende del contexto).</span><span class="sxs-lookup"><span data-stu-id="1677a-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="1677a-126">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="1677a-126">S\_OK</span></span>                                           | <span data-ttu-id="1677a-127">No se ha producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="1677a-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="1677a-128">Para escribir código que controle [los valores HRESULT](../winprog/windows-data-types.md) sólidamente, use las macros Succeeded (HR) y Failed (HR).</span><span class="sxs-lookup"><span data-stu-id="1677a-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1677a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1677a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1677a-130">Referencia de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1677a-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="1677a-131">Referencia de Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="1677a-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
