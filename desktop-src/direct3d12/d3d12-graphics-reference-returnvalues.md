---
title: Códigos de retorno de Direct3D 12
description: A continuación se muestran los códigos de retorno de las funciones de la API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705013"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="5c135-103">Códigos de retorno de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5c135-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="5c135-104">A continuación se muestran los códigos de retorno de las funciones de la API.</span><span class="sxs-lookup"><span data-stu-id="5c135-104">The following are return codes from API functions.</span></span> <span data-ttu-id="5c135-105">Para obtener más códigos de retorno, consulte [ \_ error de DXGI](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="5c135-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="5c135-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5c135-106">HRESULT</span></span>                                                                  | <span data-ttu-id="5c135-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c135-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c135-108">\_ \_ \_ No \_ se encontró el adaptador de error D3D12</span><span class="sxs-lookup"><span data-stu-id="5c135-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="5c135-109">El PSO almacenado en caché especificado se creó en un adaptador diferente y no se puede reutilizar en el adaptador actual.</span><span class="sxs-lookup"><span data-stu-id="5c135-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="5c135-110">\_Error de \_ coincidencia de versión del controlador de errores D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="5c135-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="5c135-111">El PSO almacenado en caché especificado se creó en una versión de controlador diferente y no se puede reutilizar en el adaptador actual.</span><span class="sxs-lookup"><span data-stu-id="5c135-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="5c135-112">D3DERR \_ INVALIDCALL (reemplazado por \_ error de DXGI \_ llamada no válida \_ )</span><span class="sxs-lookup"><span data-stu-id="5c135-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="5c135-113">La llamada al método no es válida.</span><span class="sxs-lookup"><span data-stu-id="5c135-113">The method call is invalid.</span></span> <span data-ttu-id="5c135-114">Por ejemplo, el parámetro de un método no puede ser un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="5c135-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="5c135-115">D3DERR \_ WASSTILLDRAWING (reemplazado por \_ error de DXGI \_ todavía se está \_ \_ dibujando)</span><span class="sxs-lookup"><span data-stu-id="5c135-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="5c135-116">La operación de blit anterior que está transfiriendo información a o desde esta superficie está incompleta.</span><span class="sxs-lookup"><span data-stu-id="5c135-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="5c135-117">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="5c135-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="5c135-118">Se intentó crear un dispositivo con la capa de depuración habilitada y la capa no está instalada.</span><span class="sxs-lookup"><span data-stu-id="5c135-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="5c135-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5c135-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="5c135-120">Se pasó un parámetro no válido a la función que devuelve.</span><span class="sxs-lookup"><span data-stu-id="5c135-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="5c135-121">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="5c135-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="5c135-122">Direct3D no pudo asignar memoria suficiente para completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="5c135-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="5c135-123">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="5c135-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="5c135-124">La llamada al método no se implementa con la combinación de parámetros pasada.</span><span class="sxs-lookup"><span data-stu-id="5c135-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="5c135-125">S \_ false</span><span class="sxs-lookup"><span data-stu-id="5c135-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="5c135-126">Valor de éxito alternativo, que indica una finalización correcta pero no estándar (el significado exacto depende del contexto).</span><span class="sxs-lookup"><span data-stu-id="5c135-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="5c135-127">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="5c135-127">S\_OK</span></span>                                                                    | <span data-ttu-id="5c135-128">No se ha producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="5c135-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5c135-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c135-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c135-130">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5c135-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 