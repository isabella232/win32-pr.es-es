---
description: Cree un bombeo de subprocesos.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Función D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003937"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="b321d-103">D3DX10CreateThreadPump función)</span><span class="sxs-lookup"><span data-stu-id="b321d-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="b321d-104">Cree un bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b321d-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="b321d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b321d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="b321d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b321d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b321d-107">*cIoThreads* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b321d-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b321d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b321d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b321d-109">Número de subprocesos de e/s que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="b321d-109">The number of I/O threads to create.</span></span> <span data-ttu-id="b321d-110">Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="b321d-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b321d-111">*cProcThreads* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b321d-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b321d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b321d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b321d-113">Número de subprocesos del proceso que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="b321d-113">The number of process threads to create.</span></span> <span data-ttu-id="b321d-114">Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="b321d-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b321d-115">*ppThreadPump* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b321d-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b321d-116">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b321d-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="b321d-117">El bombeo de subprocesos creado.</span><span class="sxs-lookup"><span data-stu-id="b321d-117">The created thread pump.</span></span> <span data-ttu-id="b321d-118">Consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b321d-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b321d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b321d-119">Return value</span></span>

<span data-ttu-id="b321d-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b321d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b321d-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b321d-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b321d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b321d-122">Remarks</span></span>

<span data-ttu-id="b321d-123">Un bombeo de subprocesos es un objeto que consume muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="b321d-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="b321d-124">Solo se debe crear un bombeo de subprocesos por aplicación.</span><span class="sxs-lookup"><span data-stu-id="b321d-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b321d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b321d-125">Requirements</span></span>



| <span data-ttu-id="b321d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b321d-126">Requirement</span></span> | <span data-ttu-id="b321d-127">Value</span><span class="sxs-lookup"><span data-stu-id="b321d-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b321d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b321d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b321d-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b321d-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b321d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b321d-130">Library</span></span><br/> | <dl> <span data-ttu-id="b321d-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b321d-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b321d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b321d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b321d-133">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="b321d-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
