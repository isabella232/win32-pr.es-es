---
description: 'Método ID3DX10Mesh::GetIndexBuffer: recupera los datos de un búfer de índice.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: Método ID3DX10Mesh::GetIndexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084033"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="29de6-103">Método ID3DX10Mesh::GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="29de6-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="29de6-104">Recupera los datos de un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="29de6-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="29de6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29de6-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="29de6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29de6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29de6-107">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29de6-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29de6-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="29de6-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="29de6-109">Dirección de un puntero a una interfaz ID3DX10MeshBuffer, que representa el búfer de índice asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="29de6-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29de6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29de6-110">Return value</span></span>

<span data-ttu-id="29de6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29de6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29de6-112">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="29de6-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29de6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29de6-113">Requirements</span></span>



| <span data-ttu-id="29de6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="29de6-114">Requirement</span></span> | <span data-ttu-id="29de6-115">Value</span><span class="sxs-lookup"><span data-stu-id="29de6-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29de6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29de6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="29de6-117"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="29de6-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="29de6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29de6-118">Library</span></span><br/> | <dl> <span data-ttu-id="29de6-119"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="29de6-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29de6-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29de6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29de6-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="29de6-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="29de6-122">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="29de6-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




