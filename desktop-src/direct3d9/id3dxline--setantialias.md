---
description: Alterna el suavizado de contorno de línea.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine:: SetAntialias (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698438"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="e0b03-103">ID3DXLine:: SetAntialias (método)</span><span class="sxs-lookup"><span data-stu-id="e0b03-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="e0b03-104">Alterna el suavizado de contorno de línea.</span><span class="sxs-lookup"><span data-stu-id="e0b03-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0b03-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="e0b03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0b03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b03-107">*bAntiAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0b03-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b03-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0b03-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0b03-109">Activa y desactiva el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="e0b03-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="e0b03-110">**True** activa el suavizado de contorno y **false** desactiva el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="e0b03-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b03-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0b03-111">Return value</span></span>

<span data-ttu-id="e0b03-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0b03-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0b03-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0b03-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0b03-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e0b03-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b03-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b03-115">Requirements</span></span>



| <span data-ttu-id="e0b03-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b03-116">Requirement</span></span> | <span data-ttu-id="e0b03-117">Value</span><span class="sxs-lookup"><span data-stu-id="e0b03-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b03-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0b03-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e0b03-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e0b03-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0b03-120">Library</span></span><br/> | <dl> <span data-ttu-id="e0b03-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0b03-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0b03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b03-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="e0b03-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="e0b03-124">**ID3DXLine::GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="e0b03-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
