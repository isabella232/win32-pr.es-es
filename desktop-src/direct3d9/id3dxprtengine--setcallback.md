---
description: Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esférico (SH) completado y proporciona al llamador la opción de anular el simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine:: SetCallBack (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707953"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="a566d-103">ID3DXPRTEngine:: SetCallBack (método)</span><span class="sxs-lookup"><span data-stu-id="a566d-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="a566d-104">Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esférico (SH) completado y proporciona al llamador la opción de anular el simulador.</span><span class="sxs-lookup"><span data-stu-id="a566d-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a566d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a566d-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="a566d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a566d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a566d-107">*pCB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a566d-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a566d-108">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="a566d-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="a566d-109">Puntero a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que calcula el porcentaje de los cálculos de SH completados.</span><span class="sxs-lookup"><span data-stu-id="a566d-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="a566d-110">La función de devolución de llamada se debe implementar para que se devuelvan \_ los elementos correctos para seguir ejecutando el simulador.</span><span class="sxs-lookup"><span data-stu-id="a566d-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="a566d-111">Cualquier otro valor anulará el simulador.</span><span class="sxs-lookup"><span data-stu-id="a566d-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="a566d-112">*Frecuencia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a566d-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a566d-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a566d-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a566d-114">Frecuencia de llamadas de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a566d-114">Frequency of callback calls.</span></span> <span data-ttu-id="a566d-115">El inverso de Frequency es aproximadamente el número de veces que se llamará a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a566d-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="a566d-116">*lpUserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a566d-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a566d-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a566d-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a566d-118">Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a566d-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="a566d-119">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a566d-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a566d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a566d-120">Return value</span></span>

<span data-ttu-id="a566d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a566d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a566d-122">El valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a566d-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a566d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a566d-123">Requirements</span></span>



| <span data-ttu-id="a566d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a566d-124">Requirement</span></span> | <span data-ttu-id="a566d-125">Value</span><span class="sxs-lookup"><span data-stu-id="a566d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a566d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a566d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a566d-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a566d-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a566d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a566d-128">Library</span></span><br/> | <dl> <span data-ttu-id="a566d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a566d-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a566d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a566d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a566d-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a566d-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
