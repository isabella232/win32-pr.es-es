---
title: Función D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Crea un efecto a partir de un efecto o archivo binario.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Función D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998526"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="bcdab-104">D3DX11CreateEffectFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="bcdab-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="bcdab-105">Crea un efecto a partir de un efecto o archivo binario.</span><span class="sxs-lookup"><span data-stu-id="bcdab-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcdab-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcdab-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="bcdab-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcdab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcdab-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="bcdab-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdab-109">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="bcdab-109">Type: **void\***</span></span>

<span data-ttu-id="bcdab-110">BLOB de datos de efectos compilados.</span><span class="sxs-lookup"><span data-stu-id="bcdab-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="bcdab-111">*DataLength*</span><span class="sxs-lookup"><span data-stu-id="bcdab-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdab-112">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bcdab-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bcdab-113">Longitud del BLOB de datos.</span><span class="sxs-lookup"><span data-stu-id="bcdab-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="bcdab-114">*FXFlags*</span><span class="sxs-lookup"><span data-stu-id="bcdab-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdab-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bcdab-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bcdab-116">No existe ninguna marca de efecto.</span><span class="sxs-lookup"><span data-stu-id="bcdab-116">No effect flags exist.</span></span> <span data-ttu-id="bcdab-117">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="bcdab-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bcdab-118">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="bcdab-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdab-119">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="bcdab-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="bcdab-120">Puntero al [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) en el que se van a crear recursos de efectos.</span><span class="sxs-lookup"><span data-stu-id="bcdab-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="bcdab-121">*ppEffect*</span><span class="sxs-lookup"><span data-stu-id="bcdab-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdab-122">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bcdab-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="bcdab-123">Dirección de la interfaz [**ID3DX11Effect**](id3dx11effect.md) que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="bcdab-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcdab-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcdab-124">Return value</span></span>

<span data-ttu-id="bcdab-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bcdab-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bcdab-126">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bcdab-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bcdab-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcdab-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bcdab-128">Debe usar el [origen de Effects 11](https://github.com/Microsoft/FX11) para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bcdab-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="bcdab-129">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bcdab-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bcdab-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcdab-130">Requirements</span></span>



| <span data-ttu-id="bcdab-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcdab-131">Requirement</span></span> | <span data-ttu-id="bcdab-132">Value</span><span class="sxs-lookup"><span data-stu-id="bcdab-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdab-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcdab-133">Header</span></span><br/> | <dl> <span data-ttu-id="bcdab-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcdab-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcdab-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcdab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcdab-136">Effects 11 funciones</span><span class="sxs-lookup"><span data-stu-id="bcdab-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

