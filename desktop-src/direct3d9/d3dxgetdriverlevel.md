---
description: Devuelve el nivel de controlador.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: Función D3DXGetDriverLevel (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718194"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="1fb2e-103">D3DXGetDriverLevel función)</span><span class="sxs-lookup"><span data-stu-id="1fb2e-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="1fb2e-104">Devuelve el nivel de controlador.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fb2e-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="1fb2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fb2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb2e-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fb2e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb2e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1fb2e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1fb2e-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb2e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fb2e-110">Return value</span></span>

<span data-ttu-id="1fb2e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fb2e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fb2e-112">El nivel de controlador.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-112">The driver level.</span></span> <span data-ttu-id="1fb2e-113">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="1fb2e-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb2e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fb2e-114">Remarks</span></span>

<span data-ttu-id="1fb2e-115">Este método devuelve la versión del controlador, que es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1fb2e-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="1fb2e-116">700: controlador de nivel de Direct3D 7</span><span class="sxs-lookup"><span data-stu-id="1fb2e-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="1fb2e-117">800: controlador de nivel de Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="1fb2e-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="1fb2e-118">900: controlador de nivel de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="1fb2e-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb2e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb2e-119">Requirements</span></span>



| <span data-ttu-id="1fb2e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb2e-120">Requirement</span></span> | <span data-ttu-id="1fb2e-121">Value</span><span class="sxs-lookup"><span data-stu-id="1fb2e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb2e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fb2e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1fb2e-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2e-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1fb2e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fb2e-124">Library</span></span><br/> | <dl> <span data-ttu-id="1fb2e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb2e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fb2e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fb2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb2e-127">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="1fb2e-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
