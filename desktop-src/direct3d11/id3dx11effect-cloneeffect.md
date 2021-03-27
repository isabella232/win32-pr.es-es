---
title: Método ID3DX11Effect CloneEffect (D3dx11effect. h)
description: Crea una copia de una interfaz de efecto.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Método CloneEffect Direct3D 11
- Método CloneEffect Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987241"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="ff63f-106">ID3DX11Effect:: CloneEffect (método)</span><span class="sxs-lookup"><span data-stu-id="ff63f-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="ff63f-107">Crea una copia de una interfaz de efecto.</span><span class="sxs-lookup"><span data-stu-id="ff63f-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff63f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff63f-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="ff63f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff63f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff63f-110">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="ff63f-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="ff63f-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff63f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ff63f-112">Marcas que afectan a la creación del efecto clonado.</span><span class="sxs-lookup"><span data-stu-id="ff63f-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="ff63f-113">Puede ser 0 o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff63f-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="ff63f-114">Marca</span><span class="sxs-lookup"><span data-stu-id="ff63f-114">Flag</span></span>                                    | <span data-ttu-id="ff63f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff63f-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff63f-116">D3DX11 \_ efecto de \_ clonación no \_ \_ Single</span><span class="sxs-lookup"><span data-stu-id="ff63f-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="ff63f-117">Omitir todos los calificadores "únicos" en cbuffers.</span><span class="sxs-lookup"><span data-stu-id="ff63f-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="ff63f-118">Todos los cbuffers tendrán sus propios [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s creados en el efecto clonado.</span><span class="sxs-lookup"><span data-stu-id="ff63f-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ff63f-119">*ppClonedEffect*</span><span class="sxs-lookup"><span data-stu-id="ff63f-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="ff63f-120">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ff63f-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="ff63f-121">Puntero a un puntero [**ID3DX11Effect**](id3dx11effect.md) que se establecerá en la copia del efecto.</span><span class="sxs-lookup"><span data-stu-id="ff63f-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff63f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff63f-122">Return value</span></span>

<span data-ttu-id="ff63f-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff63f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff63f-124">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ff63f-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff63f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff63f-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff63f-126">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="ff63f-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ff63f-127">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ff63f-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ff63f-128">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff63f-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff63f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff63f-129">Requirements</span></span>



| <span data-ttu-id="ff63f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff63f-130">Requirement</span></span> | <span data-ttu-id="ff63f-131">Value</span><span class="sxs-lookup"><span data-stu-id="ff63f-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff63f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff63f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ff63f-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff63f-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ff63f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff63f-134">Library</span></span><br/> | <dl> <span data-ttu-id="ff63f-135"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="ff63f-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff63f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff63f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff63f-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="ff63f-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

