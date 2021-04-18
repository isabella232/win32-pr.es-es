---
description: Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Función D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721511"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="1dc5c-103">D3DX10CheckVersion función)</span><span class="sxs-lookup"><span data-stu-id="1dc5c-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="1dc5c-104">Compruebe que la versión de D3DX que compiló con es la versión que está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc5c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dc5c-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="1dc5c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dc5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc5c-107">*D3DSdkVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1dc5c-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc5c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dc5c-109">Use la \_ versión del SDK de D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="1dc5c-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="1dc5c-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1dc5c-111">*D3DX10SdkVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1dc5c-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc5c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dc5c-113">Use la \_ versión del SDK de D3DX10 \_ .</span><span class="sxs-lookup"><span data-stu-id="1dc5c-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="1dc5c-114">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc5c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dc5c-115">Return value</span></span>

<span data-ttu-id="1dc5c-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1dc5c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1dc5c-117">Si la versión no coincide, la función devolverá FALSE (un número menor o igual que 0, el propio número no tiene ningún significado).</span><span class="sxs-lookup"><span data-stu-id="1dc5c-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="1dc5c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dc5c-118">Remarks</span></span>

<span data-ttu-id="1dc5c-119">Use esta función durante la inicialización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1dc5c-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="1dc5c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc5c-120">Requirements</span></span>



| <span data-ttu-id="1dc5c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc5c-121">Requirement</span></span> | <span data-ttu-id="1dc5c-122">Value</span><span class="sxs-lookup"><span data-stu-id="1dc5c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc5c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dc5c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1dc5c-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5c-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="1dc5c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dc5c-125">Library</span></span><br/> | <dl> <span data-ttu-id="1dc5c-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5c-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dc5c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dc5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc5c-128">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="1dc5c-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
