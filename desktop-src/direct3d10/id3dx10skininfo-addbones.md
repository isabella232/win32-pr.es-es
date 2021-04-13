---
description: Asigne espacio para más huesos.
ms.assetid: f2acd338-f2c2-4340-a673-f36940cf31d9
title: 'ID3DX10SkinInfo:: AddBones (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4bf9667bd25dd717c4da96c2150e7bd7c45964f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362587"
---
# <a name="id3dx10skininfoaddbones-method"></a><span data-ttu-id="b233a-103">ID3DX10SkinInfo:: AddBones (método)</span><span class="sxs-lookup"><span data-stu-id="b233a-103">ID3DX10SkinInfo::AddBones method</span></span>

<span data-ttu-id="b233a-104">Asigne espacio para más huesos.</span><span class="sxs-lookup"><span data-stu-id="b233a-104">Allocate space for more bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="b233a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b233a-105">Syntax</span></span>


```C++
HRESULT AddBones(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="b233a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b233a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b233a-107">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b233a-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b233a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b233a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b233a-109">Número de huesos que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b233a-109">The number of bones to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b233a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b233a-110">Return value</span></span>

<span data-ttu-id="b233a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b233a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b233a-112">Si este método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b233a-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b233a-113">Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b233a-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b233a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b233a-114">Requirements</span></span>



| <span data-ttu-id="b233a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b233a-115">Requirement</span></span> | <span data-ttu-id="b233a-116">Value</span><span class="sxs-lookup"><span data-stu-id="b233a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b233a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b233a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b233a-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b233a-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b233a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b233a-119">Library</span></span><br/> | <dl> <span data-ttu-id="b233a-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b233a-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b233a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b233a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b233a-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="b233a-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="b233a-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b233a-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
