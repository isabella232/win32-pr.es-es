---
title: Interfaz ID3DX11EffectStringVariable (D3dx11effect. h)
description: Una interfaz de variable de cadena tiene acceso a una variable de cadena.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- Interfaz ID3DX11EffectStringVariable Direct3D 11
- Interfaz ID3DX11EffectStringVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998323"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="6305e-105">Interfaz ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="6305e-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="6305e-106">Una interfaz de variable de cadena tiene acceso a una variable de cadena.</span><span class="sxs-lookup"><span data-stu-id="6305e-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="6305e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6305e-107">Members</span></span>

<span data-ttu-id="6305e-108">La interfaz **ID3DX11EffectStringVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6305e-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6305e-109">**ID3DX11EffectStringVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6305e-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6305e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6305e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6305e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6305e-111">Methods</span></span>

<span data-ttu-id="6305e-112">La interfaz **ID3DX11EffectStringVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6305e-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="6305e-113">Método</span><span class="sxs-lookup"><span data-stu-id="6305e-113">Method</span></span>                                                               | <span data-ttu-id="6305e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6305e-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="6305e-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="6305e-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="6305e-116">Obtiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="6305e-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="6305e-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="6305e-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="6305e-118">Obtiene una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="6305e-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6305e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6305e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6305e-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6305e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6305e-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6305e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6305e-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6305e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6305e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6305e-123">Requirements</span></span>



| <span data-ttu-id="6305e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6305e-124">Requirement</span></span> | <span data-ttu-id="6305e-125">Value</span><span class="sxs-lookup"><span data-stu-id="6305e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6305e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6305e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6305e-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6305e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6305e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6305e-128">Library</span></span><br/> | <dl> <span data-ttu-id="6305e-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6305e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6305e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6305e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6305e-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6305e-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6305e-132">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="6305e-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6305e-133">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6305e-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





