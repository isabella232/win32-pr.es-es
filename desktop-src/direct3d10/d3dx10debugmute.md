---
description: Habilitar o deshabilitar los mensajes de depuración.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Función D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718381"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="fc2cf-103">D3DX10DebugMute función)</span><span class="sxs-lookup"><span data-stu-id="fc2cf-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="fc2cf-104">Habilitar o deshabilitar los mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="fc2cf-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc2cf-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="fc2cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc2cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2cf-107">*Silenciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc2cf-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cf-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc2cf-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc2cf-109">Establézcalo en **true** para habilitar los mensajes de depuración; establézcalo en **false** para deshabilitar los mensajes de depuración.</span><span class="sxs-lookup"><span data-stu-id="fc2cf-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2cf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc2cf-110">Return value</span></span>

<span data-ttu-id="fc2cf-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc2cf-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc2cf-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fc2cf-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2cf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc2cf-113">Remarks</span></span>

<span data-ttu-id="fc2cf-114">Use esta función para deshabilitar los mensajes de error de las API de D3DX10 durante la depuración. el uso de esta función debe protegerse mediante el \_ modificador del compilador de depuración D3D10.</span><span class="sxs-lookup"><span data-stu-id="fc2cf-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="fc2cf-115">El estado predeterminado es **true** para una compilación de depuración.</span><span class="sxs-lookup"><span data-stu-id="fc2cf-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc2cf-116">Requirements</span></span>



| <span data-ttu-id="fc2cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc2cf-117">Requirement</span></span> | <span data-ttu-id="fc2cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="fc2cf-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2cf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc2cf-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fc2cf-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2cf-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="fc2cf-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc2cf-121">Library</span></span><br/> | <dl> <span data-ttu-id="fc2cf-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc2cf-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc2cf-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc2cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2cf-124">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="fc2cf-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
