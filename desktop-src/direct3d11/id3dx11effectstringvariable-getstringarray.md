---
title: Método ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Obtiene una matriz de cadenas.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Método GetStringArray Direct3D 11
- Método GetStringArray Direct3D 11, interfaz ID3DX11EffectStringVariable
- Interfaz ID3DX11EffectStringVariable Direct3D 11, método GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986814"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="95a90-106">ID3DX11EffectStringVariable:: GetStringArray (método)</span><span class="sxs-lookup"><span data-stu-id="95a90-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="95a90-107">Obtiene una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="95a90-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a90-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95a90-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="95a90-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95a90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a90-110">*ppStrings*</span><span class="sxs-lookup"><span data-stu-id="95a90-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="95a90-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="95a90-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="95a90-112">Puntero a la primera cadena de la matriz.</span><span class="sxs-lookup"><span data-stu-id="95a90-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="95a90-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="95a90-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="95a90-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95a90-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95a90-115">Desplazamiento (en número de cadenas) entre el inicio de la matriz y la primera cadena que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="95a90-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="95a90-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="95a90-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="95a90-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95a90-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95a90-118">Número de cadenas de la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="95a90-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a90-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95a90-119">Return value</span></span>

<span data-ttu-id="95a90-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95a90-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95a90-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="95a90-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95a90-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95a90-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95a90-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="95a90-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95a90-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="95a90-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95a90-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95a90-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95a90-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a90-126">Requirements</span></span>



| <span data-ttu-id="95a90-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a90-127">Requirement</span></span> | <span data-ttu-id="95a90-128">Value</span><span class="sxs-lookup"><span data-stu-id="95a90-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a90-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95a90-129">Header</span></span><br/>  | <dl> <span data-ttu-id="95a90-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a90-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95a90-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95a90-131">Library</span></span><br/> | <dl> <span data-ttu-id="95a90-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="95a90-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a90-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="95a90-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a90-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="95a90-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

