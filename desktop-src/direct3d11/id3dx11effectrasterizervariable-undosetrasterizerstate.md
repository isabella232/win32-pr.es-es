---
title: Método ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Revierte un estado de rasterizador establecido previamente.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Método UndoSetRasterizerState Direct3D 11
- Método UndoSetRasterizerState Direct3D 11, interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280521"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="09381-106">ID3DX11EffectRasterizerVariable:: UndoSetRasterizerState (método)</span><span class="sxs-lookup"><span data-stu-id="09381-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="09381-107">Revierte un estado de rasterizador establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="09381-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="09381-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09381-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="09381-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09381-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09381-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="09381-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="09381-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09381-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="09381-112">Índice en una matriz de interfaces de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="09381-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="09381-113">Si solo hay una interfaz de rasterización, use 0.</span><span class="sxs-lookup"><span data-stu-id="09381-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09381-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09381-114">Return value</span></span>

<span data-ttu-id="09381-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09381-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09381-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="09381-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09381-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09381-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09381-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="09381-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="09381-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="09381-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="09381-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="09381-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09381-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09381-121">Requirements</span></span>



| <span data-ttu-id="09381-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="09381-122">Requirement</span></span> | <span data-ttu-id="09381-123">Value</span><span class="sxs-lookup"><span data-stu-id="09381-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09381-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09381-124">Header</span></span><br/>  | <dl> <span data-ttu-id="09381-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="09381-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="09381-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09381-126">Library</span></span><br/> | <dl> <span data-ttu-id="09381-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="09381-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09381-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="09381-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09381-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="09381-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

