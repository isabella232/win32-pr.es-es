---
title: Método IsValid ID3DX11EffectTechnique (D3dx11effect. h)
description: Pruebe una técnica para ver si contiene una sintaxis válida.
ms.assetid: 599b191b-6307-4d36-b4e4-15a1ac36c65e
keywords:
- IsValid (método) Direct3D 11
- IsValid (método) Direct3D 11, ID3DX11EffectTechnique (interfaz)
- Interfaz ID3DX11EffectTechnique Direct3D 11, IsValid (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6855e1dc1073eb2ebb4484eba1f03fe4130f0b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424515"
---
# <a name="id3dx11effecttechniqueisvalid-method"></a><span data-ttu-id="43a1a-106">ID3DX11EffectTechnique:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="43a1a-106">ID3DX11EffectTechnique::IsValid method</span></span>

<span data-ttu-id="43a1a-107">Pruebe una técnica para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="43a1a-107">Test a technique to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a1a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43a1a-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="43a1a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43a1a-109">Parameters</span></span>

<span data-ttu-id="43a1a-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="43a1a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43a1a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43a1a-111">Return value</span></span>

<span data-ttu-id="43a1a-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43a1a-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43a1a-113">**True** si la sintaxis del código es válida; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="43a1a-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a1a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43a1a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43a1a-115">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="43a1a-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="43a1a-116">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="43a1a-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="43a1a-117">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="43a1a-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43a1a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a1a-118">Requirements</span></span>



| <span data-ttu-id="43a1a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a1a-119">Requirement</span></span> | <span data-ttu-id="43a1a-120">Value</span><span class="sxs-lookup"><span data-stu-id="43a1a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a1a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43a1a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="43a1a-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a1a-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="43a1a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43a1a-123">Library</span></span><br/> | <dl> <span data-ttu-id="43a1a-124"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="43a1a-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a1a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="43a1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a1a-126">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="43a1a-126">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

