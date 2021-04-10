---
description: Activa o desactiva todos los resultados de depuración de D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Función D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280325"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="52c79-103">D3DXDebugMute función)</span><span class="sxs-lookup"><span data-stu-id="52c79-103">D3DXDebugMute function</span></span>

<span data-ttu-id="52c79-104">Activa o desactiva todos los resultados de depuración de D3DX.</span><span class="sxs-lookup"><span data-stu-id="52c79-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52c79-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="52c79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52c79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c79-107">*Silenciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52c79-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c79-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52c79-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52c79-109">Si es **true**, la salida del depurador se detiene; Si es **false**, la salida de depuración está habilitada.</span><span class="sxs-lookup"><span data-stu-id="52c79-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c79-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52c79-110">Return value</span></span>

<span data-ttu-id="52c79-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52c79-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52c79-112">Devuelve el valor anterior de silenciar.</span><span class="sxs-lookup"><span data-stu-id="52c79-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c79-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c79-113">Requirements</span></span>



| <span data-ttu-id="52c79-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c79-114">Requirement</span></span> | <span data-ttu-id="52c79-115">Value</span><span class="sxs-lookup"><span data-stu-id="52c79-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52c79-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52c79-116">Header</span></span><br/>  | <dl> <span data-ttu-id="52c79-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c79-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="52c79-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52c79-118">Library</span></span><br/> | <dl> <span data-ttu-id="52c79-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52c79-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52c79-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="52c79-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c79-121">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="52c79-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
