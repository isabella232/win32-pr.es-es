---
description: Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Función D3DXCheckVersion (D3dx9core. h)
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649424"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="b9406-103">D3DXCheckVersion función)</span><span class="sxs-lookup"><span data-stu-id="b9406-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="b9406-104">Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b9406-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9406-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9406-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="b9406-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9406-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9406-107">*D3DSDKVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9406-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9406-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9406-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9406-109">Use la \_ versión del SDK de D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="b9406-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="b9406-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="b9406-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b9406-111">*D3DXSDKVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9406-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9406-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9406-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9406-113">Use la \_ versión del SDK de D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="b9406-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="b9406-114">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="b9406-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9406-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9406-115">Return value</span></span>

<span data-ttu-id="b9406-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9406-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9406-117">Devuelve **true** si la versión de D3DX que compiló es la versión con la que se está ejecutando; de lo contrario, se devuelve **false** .</span><span class="sxs-lookup"><span data-stu-id="b9406-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9406-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9406-118">Remarks</span></span>

<span data-ttu-id="b9406-119">Use esta función durante la inicialización de la aplicación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b9406-119">Use this function during the initialization of your application like this:</span></span>


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



<span data-ttu-id="b9406-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) para comprobar que está instalado el tiempo de ejecución correcto.</span><span class="sxs-lookup"><span data-stu-id="b9406-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9406-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9406-121">Requirements</span></span>



| <span data-ttu-id="b9406-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9406-122">Requirement</span></span> | <span data-ttu-id="b9406-123">Value</span><span class="sxs-lookup"><span data-stu-id="b9406-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9406-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9406-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b9406-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9406-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b9406-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9406-126">Library</span></span><br/> | <dl> <span data-ttu-id="b9406-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9406-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9406-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9406-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9406-129">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="b9406-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
