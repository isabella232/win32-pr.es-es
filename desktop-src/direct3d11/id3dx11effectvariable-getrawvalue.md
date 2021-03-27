---
title: Método ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: Obtener datos.
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Método GetRawValue Direct3D 11
- Método GetRawValue Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987145"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a><span data-ttu-id="c50d0-106">ID3DX11EffectVariable:: GetRawValue (método)</span><span class="sxs-lookup"><span data-stu-id="c50d0-106">ID3DX11EffectVariable::GetRawValue method</span></span>

<span data-ttu-id="c50d0-107">Obtener datos.</span><span class="sxs-lookup"><span data-stu-id="c50d0-107">Get data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50d0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c50d0-108">Syntax</span></span>


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="c50d0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c50d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50d0-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="c50d0-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d0-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="c50d0-111">Type: **void\***</span></span>

<span data-ttu-id="c50d0-112">Puntero a la variable.</span><span class="sxs-lookup"><span data-stu-id="c50d0-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="c50d0-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c50d0-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d0-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c50d0-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c50d0-115">Desplazamiento, en bytes, desde el principio del puntero a los datos.</span><span class="sxs-lookup"><span data-stu-id="c50d0-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="c50d0-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="c50d0-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d0-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c50d0-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c50d0-118">Número de bytes que se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="c50d0-118">The number of bytes to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50d0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c50d0-119">Return value</span></span>

<span data-ttu-id="c50d0-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c50d0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c50d0-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c50d0-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c50d0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c50d0-122">Remarks</span></span>

<span data-ttu-id="c50d0-123">Este método no realiza ninguna comprobación de conversión o de tipo; por lo tanto, es una manera muy rápida de tener acceso a los elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c50d0-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="c50d0-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="c50d0-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c50d0-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c50d0-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c50d0-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c50d0-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c50d0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c50d0-127">Requirements</span></span>



| <span data-ttu-id="c50d0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c50d0-128">Requirement</span></span> | <span data-ttu-id="c50d0-129">Value</span><span class="sxs-lookup"><span data-stu-id="c50d0-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50d0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c50d0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c50d0-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50d0-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c50d0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c50d0-132">Library</span></span><br/> | <dl> <span data-ttu-id="c50d0-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="c50d0-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50d0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c50d0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50d0-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c50d0-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

