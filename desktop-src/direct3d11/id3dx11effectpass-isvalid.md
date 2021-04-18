---
title: Método IsValid ID3DX11EffectPass (D3dx11effect. h)
description: Pruebe un paso para ver si contiene una sintaxis válida.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- IsValid (método) Direct3D 11
- IsValid (método) Direct3D 11, ID3DX11EffectPass (interfaz)
- Interfaz ID3DX11EffectPass Direct3D 11, IsValid (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986917"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="52967-106">ID3DX11EffectPass:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="52967-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="52967-107">Pruebe un paso para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="52967-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="52967-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52967-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="52967-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52967-109">Parameters</span></span>

<span data-ttu-id="52967-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="52967-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52967-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52967-111">Return value</span></span>

<span data-ttu-id="52967-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="52967-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="52967-113">**True** si la sintaxis del código es válida; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="52967-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="52967-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52967-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52967-115">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="52967-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="52967-116">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="52967-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="52967-117">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="52967-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52967-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52967-118">Requirements</span></span>



| <span data-ttu-id="52967-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52967-119">Requirement</span></span> | <span data-ttu-id="52967-120">Value</span><span class="sxs-lookup"><span data-stu-id="52967-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52967-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52967-121">Header</span></span><br/>  | <dl> <span data-ttu-id="52967-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="52967-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="52967-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52967-123">Library</span></span><br/> | <dl> <span data-ttu-id="52967-124"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="52967-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52967-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="52967-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52967-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="52967-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

