---
title: Método IsValid ID3DX11Effect (D3dx11effect. h)
description: Pruebe un efecto para ver si contiene una sintaxis válida. | Método IsValid ID3DX11Effect (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- IsValid (método) Direct3D 11
- IsValid (método) Direct3D 11, ID3DX11Effect (interfaz)
- Interfaz ID3DX11Effect Direct3D 11, IsValid (método)
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998605"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="2b86f-107">ID3DX11Effect:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="2b86f-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="2b86f-108">Pruebe un efecto para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="2b86f-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b86f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b86f-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="2b86f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b86f-110">Parameters</span></span>

<span data-ttu-id="2b86f-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2b86f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b86f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b86f-112">Return value</span></span>

<span data-ttu-id="2b86f-113">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2b86f-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2b86f-114">**True** si la sintaxis del código es válida; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2b86f-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b86f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b86f-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b86f-116">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="2b86f-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2b86f-117">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="2b86f-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2b86f-118">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2b86f-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b86f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b86f-119">Requirements</span></span>



| <span data-ttu-id="2b86f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b86f-120">Requirement</span></span> | <span data-ttu-id="2b86f-121">Value</span><span class="sxs-lookup"><span data-stu-id="2b86f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b86f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b86f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2b86f-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b86f-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2b86f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b86f-124">Library</span></span><br/> | <dl> <span data-ttu-id="2b86f-125"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="2b86f-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b86f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b86f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b86f-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2b86f-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

