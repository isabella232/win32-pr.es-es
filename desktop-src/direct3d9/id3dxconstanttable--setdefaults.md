---
description: Establece las constantes en sus valores predeterminados. Los valores predeterminados se declaran en las declaraciones de variable en el sombreador.
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'ID3DXConstantTable:: SetDefaults (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821119"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="42774-104">ID3DXConstantTable:: SetDefaults (método)</span><span class="sxs-lookup"><span data-stu-id="42774-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="42774-105">Establece las constantes en sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="42774-105">Sets the constants to their default values.</span></span> <span data-ttu-id="42774-106">Los valores predeterminados se declaran en las declaraciones de variable en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="42774-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="42774-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42774-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="42774-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42774-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42774-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42774-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42774-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="42774-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="42774-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="42774-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42774-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42774-112">Return value</span></span>

<span data-ttu-id="42774-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42774-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42774-114">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42774-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42774-115">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="42774-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="42774-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42774-116">Requirements</span></span>



| <span data-ttu-id="42774-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42774-117">Requirement</span></span> | <span data-ttu-id="42774-118">Value</span><span class="sxs-lookup"><span data-stu-id="42774-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42774-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42774-119">Header</span></span><br/>  | <dl> <span data-ttu-id="42774-120"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="42774-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="42774-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42774-121">Library</span></span><br/> | <dl> <span data-ttu-id="42774-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42774-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="42774-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="42774-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42774-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="42774-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
