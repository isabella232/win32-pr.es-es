---
title: Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998473"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="bfb32-107">ID3DX11EffectGroup:: GetAnnotationByName (método)</span><span class="sxs-lookup"><span data-stu-id="bfb32-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="bfb32-108">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="bfb32-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb32-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfb32-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="bfb32-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfb32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb32-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="bfb32-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="bfb32-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bfb32-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bfb32-113">El nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="bfb32-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb32-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfb32-114">Return value</span></span>

<span data-ttu-id="bfb32-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="bfb32-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="bfb32-116">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="bfb32-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="bfb32-117">Tenga en cuenta que si no se encuentra la anotación, el **ID3DX11EffectVariable** devuelto estará vacío.</span><span class="sxs-lookup"><span data-stu-id="bfb32-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="bfb32-118">Se debe llamar al método [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) para determinar si se encontró la anotación.</span><span class="sxs-lookup"><span data-stu-id="bfb32-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb32-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb32-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bfb32-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="bfb32-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bfb32-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bfb32-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bfb32-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bfb32-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bfb32-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb32-123">Requirements</span></span>



| <span data-ttu-id="bfb32-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb32-124">Requirement</span></span> | <span data-ttu-id="bfb32-125">Value</span><span class="sxs-lookup"><span data-stu-id="bfb32-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb32-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfb32-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bfb32-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfb32-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bfb32-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfb32-128">Library</span></span><br/> | <dl> <span data-ttu-id="bfb32-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="bfb32-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb32-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfb32-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb32-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="bfb32-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

