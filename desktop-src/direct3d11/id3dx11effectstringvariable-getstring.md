---
title: Método GetString ID3DX11EffectStringVariable (D3dx11effect. h)
description: Obtiene la cadena.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- GetString (método) Direct3D 11
- Método GetString Direct3D 11, interfaz ID3DX11EffectStringVariable
- Interfaz ID3DX11EffectStringVariable Direct3D 11, GetString (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986815"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="e307d-106">ID3DX11EffectStringVariable:: GetString (método)</span><span class="sxs-lookup"><span data-stu-id="e307d-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="e307d-107">Obtiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="e307d-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e307d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e307d-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="e307d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e307d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e307d-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="e307d-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="e307d-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="e307d-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e307d-112">Puntero a la cadena.</span><span class="sxs-lookup"><span data-stu-id="e307d-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e307d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e307d-113">Return value</span></span>

<span data-ttu-id="e307d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e307d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e307d-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e307d-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e307d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e307d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e307d-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="e307d-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e307d-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e307d-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e307d-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e307d-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e307d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e307d-120">Requirements</span></span>



| <span data-ttu-id="e307d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e307d-121">Requirement</span></span> | <span data-ttu-id="e307d-122">Value</span><span class="sxs-lookup"><span data-stu-id="e307d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e307d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e307d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e307d-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e307d-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e307d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e307d-125">Library</span></span><br/> | <dl> <span data-ttu-id="e307d-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="e307d-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e307d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e307d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e307d-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="e307d-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

