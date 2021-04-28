---
description: 'Función D3DXCheckVersion: compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Función D3DXCheckVersion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 077d64a67a46080a0f7ac9194c684f6fe8470453
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115983"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="73ced-103">Función D3DXCheckVersion</span><span class="sxs-lookup"><span data-stu-id="73ced-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="73ced-104">Compruebe que la versión de D3DX con la que ha compilado es la versión que está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="73ced-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ced-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73ced-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="73ced-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73ced-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ced-107">*D3DSDKVersion* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="73ced-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ced-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ced-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ced-109">Use D3D \_ SDK \_ VERSION.</span><span class="sxs-lookup"><span data-stu-id="73ced-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="73ced-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="73ced-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="73ced-111">*D3DXSDKVersion* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="73ced-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ced-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ced-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ced-113">Use D3DX \_ SDK \_ VERSION.</span><span class="sxs-lookup"><span data-stu-id="73ced-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="73ced-114">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="73ced-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ced-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73ced-115">Return value</span></span>

<span data-ttu-id="73ced-116">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73ced-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73ced-117">Devuelve **TRUE** si la versión de D3DX con la que se compiló es la versión con la que se está ejecutando; De lo contrario, se devuelve **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="73ced-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="73ced-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73ced-118">Remarks</span></span>

<span data-ttu-id="73ced-119">Use esta función durante la inicialización de la aplicación de esta forma:</span><span class="sxs-lookup"><span data-stu-id="73ced-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="73ced-120">Use [**Direct3DCreate9 para**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) comprobar que está instalado el tiempo de ejecución correcto.</span><span class="sxs-lookup"><span data-stu-id="73ced-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ced-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ced-121">Requirements</span></span>



| <span data-ttu-id="73ced-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ced-122">Requirement</span></span> | <span data-ttu-id="73ced-123">Value</span><span class="sxs-lookup"><span data-stu-id="73ced-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ced-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73ced-124">Header</span></span><br/>  | <dl> <span data-ttu-id="73ced-125"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="73ced-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="73ced-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73ced-126">Library</span></span><br/> | <dl> <span data-ttu-id="73ced-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ced-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73ced-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73ced-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ced-129">De uso general Functions</span><span class="sxs-lookup"><span data-stu-id="73ced-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
