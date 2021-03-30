---
description: Inicia una técnica activa.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect:: Begin (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280353"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="a25bf-103">ID3DXEffect:: Begin (método)</span><span class="sxs-lookup"><span data-stu-id="a25bf-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="a25bf-104">Inicia una técnica activa.</span><span class="sxs-lookup"><span data-stu-id="a25bf-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="a25bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a25bf-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a25bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a25bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25bf-107">*pPasses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a25bf-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a25bf-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a25bf-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a25bf-109">Puntero a un valor devuelto que indica el número de pasos necesarios para representar la técnica actual.</span><span class="sxs-lookup"><span data-stu-id="a25bf-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="a25bf-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a25bf-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a25bf-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a25bf-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a25bf-112">DWORD que determina si se guarda y restaura el estado modificado por un efecto.</span><span class="sxs-lookup"><span data-stu-id="a25bf-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="a25bf-113">El valor predeterminado 0 especifica que **ID3DXEffect:: Begin** y [**ID3DXEffect:: end**](id3dxeffect--end.md) guardarán y restaurarán todos los Estados modificados por el efecto (incluidas las constantes de sombreador de píxeles y vértices).</span><span class="sxs-lookup"><span data-stu-id="a25bf-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="a25bf-114">Las marcas válidas pueden verse en el [Estado de efecto guardar y restaurar](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a25bf-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a25bf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a25bf-115">Return value</span></span>

<span data-ttu-id="a25bf-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a25bf-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a25bf-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a25bf-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a25bf-118">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a25bf-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a25bf-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a25bf-119">Remarks</span></span>

<span data-ttu-id="a25bf-120">Una aplicación establece una técnica activa en el sistema de efectos llamando a **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="a25bf-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="a25bf-121">El sistema de efecto responde capturando todo el estado de canalización que se puede cambiar mediante la técnica en un bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="a25bf-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="a25bf-122">Una aplicación señala el final de una técnica mediante una llamada a [**ID3DXEffect:: end**](id3dxeffect--end.md), que usa el bloque de estado para restaurar el estado original.</span><span class="sxs-lookup"><span data-stu-id="a25bf-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="a25bf-123">Por lo tanto, el sistema de efectos se encarga de guardar el estado cuando se activa una técnica y restaurar el estado cuando finaliza una técnica.</span><span class="sxs-lookup"><span data-stu-id="a25bf-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="a25bf-124">Si decide deshabilitar esta funcionalidad de guardar y restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a25bf-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="a25bf-125">En el par **ID3DXEffect:: Begin** y [**ID3DXEffect:: end**](id3dxeffect--end.md) , una aplicación usa [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) para establecer el paso activo, [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) si se produce algún cambio de estado después de que se activara el paso, y [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) para finalizar el paso activo.</span><span class="sxs-lookup"><span data-stu-id="a25bf-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a25bf-126">Requirements</span></span>



| <span data-ttu-id="a25bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a25bf-127">Requirement</span></span> | <span data-ttu-id="a25bf-128">Value</span><span class="sxs-lookup"><span data-stu-id="a25bf-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25bf-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a25bf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a25bf-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25bf-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a25bf-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a25bf-131">Library</span></span><br/> | <dl> <span data-ttu-id="a25bf-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a25bf-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a25bf-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a25bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25bf-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="a25bf-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
