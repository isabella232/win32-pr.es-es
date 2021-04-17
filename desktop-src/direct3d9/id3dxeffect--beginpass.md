---
description: Comienza un paso, dentro de la técnica activa.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect:: BeginPass (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718241"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="dcdc3-103">ID3DXEffect:: BeginPass (método)</span><span class="sxs-lookup"><span data-stu-id="dcdc3-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="dcdc3-104">Comienza un paso, dentro de la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcdc3-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="dcdc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcdc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcdc3-107">*Pass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcdc3-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcdc3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcdc3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcdc3-109">Índice de entero de base cero de la técnica.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcdc3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcdc3-110">Return value</span></span>

<span data-ttu-id="dcdc3-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcdc3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcdc3-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcdc3-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcdc3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcdc3-114">Remarks</span></span>

<span data-ttu-id="dcdc3-115">Una aplicación establece un paso activo (dentro de una técnica activa) en el sistema de efectos llamando a **ID3DXEffect:: BeginPass**.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="dcdc3-116">Una aplicación señala el final del paso activo mediante una llamada a [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="dcdc3-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="dcdc3-117">**ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** deben aparecer en un par coincidente, dentro de un par coincidente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y [**ID3DXEffect:: end**](id3dxeffect--end.md) calls.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="dcdc3-118">Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**Effect:: setx**](id3dxeffect.md) dentro de un par de coincidencia **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) , la aplicación debe llamar a [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) para establecer la actualización del dispositivo con los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="dcdc3-119">Si no se produce ningún cambio de estado dentro de un par de coincidencia **ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** , no es necesario llamar a **ID3DXEffect:: commitChanges**.</span><span class="sxs-lookup"><span data-stu-id="dcdc3-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcdc3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcdc3-120">Requirements</span></span>



| <span data-ttu-id="dcdc3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcdc3-121">Requirement</span></span> | <span data-ttu-id="dcdc3-122">Value</span><span class="sxs-lookup"><span data-stu-id="dcdc3-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdc3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcdc3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dcdc3-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcdc3-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dcdc3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcdc3-125">Library</span></span><br/> | <dl> <span data-ttu-id="dcdc3-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcdc3-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dcdc3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcdc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdc3-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="dcdc3-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
