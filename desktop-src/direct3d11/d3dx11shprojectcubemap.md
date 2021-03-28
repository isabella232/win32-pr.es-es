---
title: Función D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca matemática de armónicos esféricos, SHProjectCubeMap.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Función D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998496"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="6f944-105">D3DX11SHProjectCubeMap función)</span><span class="sxs-lookup"><span data-stu-id="6f944-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="6f944-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="6f944-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="6f944-107">En lugar de usar esta función, se recomienda usar la biblioteca [matemática de armónicos esféricos](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) , **SHProjectCubeMap**.</span><span class="sxs-lookup"><span data-stu-id="6f944-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="6f944-108">Proyecta una función representada en un mapa de cubo en armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="6f944-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f944-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f944-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="6f944-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f944-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f944-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="6f944-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-112">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="6f944-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="6f944-113">Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="6f944-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="6f944-114">*Pedido*</span><span class="sxs-lookup"><span data-stu-id="6f944-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6f944-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6f944-116">Orden de la evaluación de SH, genera coeficientes de pedido ^ 2 cuyo grado es el orden 1.</span><span class="sxs-lookup"><span data-stu-id="6f944-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="6f944-117">El intervalo válido está comprendido entre 2 y 6.</span><span class="sxs-lookup"><span data-stu-id="6f944-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="6f944-118">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="6f944-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-119">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="6f944-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="6f944-120">Un puntero a un [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa un mapa que se va a proyectar en armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="6f944-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="6f944-121">*pROut*</span><span class="sxs-lookup"><span data-stu-id="6f944-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-122">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6f944-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6f944-123">Salida SH vector para rojo.</span><span class="sxs-lookup"><span data-stu-id="6f944-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="6f944-124">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="6f944-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6f944-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6f944-126">Salida SH vector para verde.</span><span class="sxs-lookup"><span data-stu-id="6f944-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="6f944-127">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="6f944-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="6f944-128">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="6f944-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6f944-129">Salida SH vector para azul.</span><span class="sxs-lookup"><span data-stu-id="6f944-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f944-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f944-130">Return value</span></span>

<span data-ttu-id="6f944-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f944-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f944-132">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6f944-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f944-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f944-133">Requirements</span></span>



| <span data-ttu-id="6f944-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f944-134">Requirement</span></span> | <span data-ttu-id="6f944-135">Value</span><span class="sxs-lookup"><span data-stu-id="6f944-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f944-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f944-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6f944-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f944-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6f944-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f944-138">Library</span></span><br/> | <dl> <span data-ttu-id="6f944-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f944-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6f944-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f944-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f944-141">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="6f944-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

