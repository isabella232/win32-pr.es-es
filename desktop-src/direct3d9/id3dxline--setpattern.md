---
description: Aplica un patrón punteado a la línea.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'ID3DXLine:: SetPattern (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157236"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="153a9-103">ID3DXLine:: SetPattern (método)</span><span class="sxs-lookup"><span data-stu-id="153a9-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="153a9-104">Aplica un patrón punteado a la línea.</span><span class="sxs-lookup"><span data-stu-id="153a9-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="153a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="153a9-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="153a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="153a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153a9-107">*dwPattern* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="153a9-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153a9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="153a9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="153a9-109">Describe el patrón punteado: 1 es opaco, 0 es transparente.</span><span class="sxs-lookup"><span data-stu-id="153a9-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153a9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="153a9-110">Return value</span></span>

<span data-ttu-id="153a9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="153a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="153a9-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="153a9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="153a9-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="153a9-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="153a9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="153a9-114">Requirements</span></span>



| <span data-ttu-id="153a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="153a9-115">Requirement</span></span> | <span data-ttu-id="153a9-116">Value</span><span class="sxs-lookup"><span data-stu-id="153a9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="153a9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="153a9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="153a9-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="153a9-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="153a9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="153a9-119">Library</span></span><br/> | <dl> <span data-ttu-id="153a9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="153a9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="153a9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="153a9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153a9-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="153a9-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
