---
title: Método IsValid ID3DX11EffectVariable (D3dx11effect. h)
description: Comparar el tipo de datos con los datos almacenados.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- IsValid (método) Direct3D 11
- IsValid (método) Direct3D 11, ID3DX11EffectVariable (interfaz)
- Interfaz ID3DX11EffectVariable Direct3D 11, IsValid (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998641"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="5c9b1-106">ID3DX11EffectVariable:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="5c9b1-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="5c9b1-107">Comparar el tipo de datos con los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c9b1-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="5c9b1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c9b1-109">Parameters</span></span>

<span data-ttu-id="5c9b1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c9b1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c9b1-111">Return value</span></span>

<span data-ttu-id="5c9b1-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c9b1-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c9b1-113">**True** si la sintaxis es válida; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c9b1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c9b1-114">Remarks</span></span>

<span data-ttu-id="5c9b1-115">Este método comprueba que el tipo de datos coincide con los datos almacenados después de convertir una interfaz en otra (mediante cualquiera de los métodos as).</span><span class="sxs-lookup"><span data-stu-id="5c9b1-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="5c9b1-116">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5c9b1-117">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5c9b1-118">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5c9b1-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c9b1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c9b1-119">Requirements</span></span>



| <span data-ttu-id="5c9b1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9b1-120">Requirement</span></span> | <span data-ttu-id="5c9b1-121">Value</span><span class="sxs-lookup"><span data-stu-id="5c9b1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9b1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c9b1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5c9b1-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c9b1-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5c9b1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c9b1-124">Library</span></span><br/> | <dl> <span data-ttu-id="5c9b1-125"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5c9b1-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9b1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c9b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9b1-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="5c9b1-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

