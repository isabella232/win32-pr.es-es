---
title: D3DX11_PASS_SHADER_DESC estructura (D3dx11effect. h)
description: Describe un paso de efecto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987199"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="aa239-104">D3DX11 \_ ( \_ estructura de Desc del sombreador de paso) \_</span><span class="sxs-lookup"><span data-stu-id="aa239-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="aa239-105">Describe un paso de efecto.</span><span class="sxs-lookup"><span data-stu-id="aa239-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa239-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa239-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="aa239-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa239-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa239-108">**pShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="aa239-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="aa239-109">Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa239-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="aa239-110">Variable de la que procede este sombreador.</span><span class="sxs-lookup"><span data-stu-id="aa239-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="aa239-111">**ShaderIndex**</span><span class="sxs-lookup"><span data-stu-id="aa239-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="aa239-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa239-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="aa239-113">Elemento de pShaderVariable (si es una matriz) o 0 si no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="aa239-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa239-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa239-114">Remarks</span></span>

<span data-ttu-id="aa239-115">D3DX11 \_ Pass \_ Shader \_ desc se usa con los métodos [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.</span><span class="sxs-lookup"><span data-stu-id="aa239-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="aa239-116">Si se trata de una asignación de sombreador en línea, la interfaz devuelta será una variable de sombreador anónima, que no se puede recuperar de ninguna otra manera.</span><span class="sxs-lookup"><span data-stu-id="aa239-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="aa239-117">Su nombre en la descripción de la variable será "$Anonymous".</span><span class="sxs-lookup"><span data-stu-id="aa239-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="aa239-118">Si no hay ninguna asignación de este tipo en el bloque Pass, pShaderVariable! = **null**, pero pShaderVariable->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="aa239-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa239-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa239-119">Requirements</span></span>



| <span data-ttu-id="aa239-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa239-120">Requirement</span></span> | <span data-ttu-id="aa239-121">Value</span><span class="sxs-lookup"><span data-stu-id="aa239-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa239-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa239-122">Header</span></span><br/> | <dl> <span data-ttu-id="aa239-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa239-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa239-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa239-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa239-125">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="aa239-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

