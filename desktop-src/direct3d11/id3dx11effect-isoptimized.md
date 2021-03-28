---
title: Método ID3DX11Effect IsOptimized (D3dx11effect. h)
description: Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Método IsOptimized Direct3D 11
- Método IsOptimized Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método IsOptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362707"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="926c2-106">ID3DX11Effect:: IsOptimized (método)</span><span class="sxs-lookup"><span data-stu-id="926c2-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="926c2-107">Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.</span><span class="sxs-lookup"><span data-stu-id="926c2-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="926c2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="926c2-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="926c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="926c2-109">Parameters</span></span>

<span data-ttu-id="926c2-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="926c2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="926c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="926c2-111">Return value</span></span>

<span data-ttu-id="926c2-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="926c2-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="926c2-113">**True** si el efecto está optimizado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="926c2-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="926c2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="926c2-114">Remarks</span></span>

<span data-ttu-id="926c2-115">Un efecto usa el espacio de memoria de dos maneras diferentes: almacenar la información requerida por el motor en tiempo de ejecución para ejecutar un efecto y almacenar los metadatos necesarios para reflejar información de nuevo en una aplicación mediante la API.</span><span class="sxs-lookup"><span data-stu-id="926c2-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="926c2-116">Puede minimizar la cantidad de memoria requerida por un efecto llamando a [**ID3DX11Effect:: Optimize**](id3dx11effect-optimize.md) , que quita los metadatos de reflexión de la memoria.</span><span class="sxs-lookup"><span data-stu-id="926c2-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="926c2-117">Por supuesto, los métodos de API para leer variables dejarán de funcionar una vez que se hayan quitado los datos de reflexión.</span><span class="sxs-lookup"><span data-stu-id="926c2-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="926c2-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="926c2-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="926c2-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="926c2-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="926c2-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="926c2-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="926c2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="926c2-121">Requirements</span></span>



| <span data-ttu-id="926c2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="926c2-122">Requirement</span></span> | <span data-ttu-id="926c2-123">Value</span><span class="sxs-lookup"><span data-stu-id="926c2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="926c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="926c2-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="926c2-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="926c2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="926c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="926c2-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="926c2-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926c2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="926c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926c2-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="926c2-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

