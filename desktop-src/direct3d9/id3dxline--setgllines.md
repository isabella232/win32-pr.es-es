---
description: Alterna el modo para dibujar líneas de estilo OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'ID3DXLine:: SetGLLines (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914822"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="01528-103">ID3DXLine:: SetGLLines (método)</span><span class="sxs-lookup"><span data-stu-id="01528-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="01528-104">Alterna el modo para dibujar líneas de estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="01528-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="01528-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01528-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="01528-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01528-107">*bGLLines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01528-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01528-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01528-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01528-109">Alterna el dibujo de línea de estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="01528-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="01528-110">**True** habilita las líneas de estilo OpenGL y **false** habilita las líneas de estilo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01528-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01528-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01528-111">Return value</span></span>

<span data-ttu-id="01528-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01528-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01528-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01528-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01528-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="01528-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="01528-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01528-115">Requirements</span></span>



| <span data-ttu-id="01528-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="01528-116">Requirement</span></span> | <span data-ttu-id="01528-117">Value</span><span class="sxs-lookup"><span data-stu-id="01528-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01528-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01528-118">Header</span></span><br/>  | <dl> <span data-ttu-id="01528-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="01528-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="01528-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01528-120">Library</span></span><br/> | <dl> <span data-ttu-id="01528-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01528-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01528-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="01528-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01528-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="01528-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
