---
title: Método Optimize ID3DX11Effect (D3dx11effect. h)
description: Minimizar la cantidad de memoria necesaria para un efecto.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimizar el método Direct3D 11
- Optimizar el método Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998604"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="dab5c-106">ID3DX11Effect:: Optimize (método)</span><span class="sxs-lookup"><span data-stu-id="dab5c-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="dab5c-107">Minimizar la cantidad de memoria necesaria para un efecto.</span><span class="sxs-lookup"><span data-stu-id="dab5c-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dab5c-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="dab5c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dab5c-109">Parameters</span></span>

<span data-ttu-id="dab5c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dab5c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dab5c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dab5c-111">Return value</span></span>

<span data-ttu-id="dab5c-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dab5c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dab5c-113">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dab5c-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dab5c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dab5c-114">Remarks</span></span>

<span data-ttu-id="dab5c-115">Un efecto usa el espacio de memoria de dos maneras diferentes: almacenar la información requerida por el motor en tiempo de ejecución para ejecutar un efecto y almacenar los metadatos necesarios para reflejar información de nuevo en una aplicación mediante la API.</span><span class="sxs-lookup"><span data-stu-id="dab5c-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="dab5c-116">Puede minimizar la cantidad de memoria requerida por un efecto llamando a **ID3DX11Effect:: Optimize** , que quita los metadatos de reflexión de la memoria.</span><span class="sxs-lookup"><span data-stu-id="dab5c-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="dab5c-117">Los métodos de API para leer variables dejarán de funcionar una vez que se hayan quitado los datos de reflexión.</span><span class="sxs-lookup"><span data-stu-id="dab5c-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="dab5c-118">Se producirá un error en los siguientes métodos después de haber llamado a Optimize en un efecto.</span><span class="sxs-lookup"><span data-stu-id="dab5c-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="dab5c-119">**ID3DX11Effect::GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="dab5c-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="dab5c-120">**ID3DX11Effect::GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="dab5c-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="dab5c-121">**ID3DX11Effect::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="dab5c-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="dab5c-122">**ID3DX11Effect:: GetDevice**</span><span class="sxs-lookup"><span data-stu-id="dab5c-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="dab5c-123">**ID3DX11Effect::GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="dab5c-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="dab5c-124">**ID3DX11Effect::GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="dab5c-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="dab5c-125">**ID3DX11Effect::GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="dab5c-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="dab5c-126">**ID3DX11Effect::GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="dab5c-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="dab5c-127">**ID3DX11Effect::GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="dab5c-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="dab5c-128">Las referencias recuperadas con estos métodos antes de llamar a **ID3DX11Effect:: Optimize** siguen siendo válidas después de llamar a **ID3DX11Effect:: Optimize** .</span><span class="sxs-lookup"><span data-stu-id="dab5c-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="dab5c-129">Esto permite a la aplicación obtener todas las variables, técnicas y pases que usará, llamar a Optimize y, a continuación, usar el efecto.</span><span class="sxs-lookup"><span data-stu-id="dab5c-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="dab5c-130">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="dab5c-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="dab5c-131">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="dab5c-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="dab5c-132">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="dab5c-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dab5c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dab5c-133">Requirements</span></span>



| <span data-ttu-id="dab5c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dab5c-134">Requirement</span></span> | <span data-ttu-id="dab5c-135">Value</span><span class="sxs-lookup"><span data-stu-id="dab5c-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab5c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dab5c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="dab5c-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab5c-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dab5c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dab5c-138">Library</span></span><br/> | <dl> <span data-ttu-id="dab5c-139"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="dab5c-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab5c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="dab5c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab5c-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="dab5c-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





