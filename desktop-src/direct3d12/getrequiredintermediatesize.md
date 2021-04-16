---
title: Función GetRequiredIntermediateSize (D3dx12. h)
description: Devuelve el tamaño necesario de un búfer que se va a utilizar para la carga de datos.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize función)
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649429"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="4cc22-104">GetRequiredIntermediateSize función)</span><span class="sxs-lookup"><span data-stu-id="4cc22-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="4cc22-105">Devuelve el tamaño necesario de un búfer que se va a utilizar para la carga de datos.</span><span class="sxs-lookup"><span data-stu-id="4cc22-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc22-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cc22-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="4cc22-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cc22-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc22-108">*pDestinationResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4cc22-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc22-109">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="4cc22-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="4cc22-110">Puntero a la interfaz [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa el recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="4cc22-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="4cc22-111">*FirstSubresource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4cc22-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc22-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc22-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cc22-113">Índice del primer subrecurso del recurso.</span><span class="sxs-lookup"><span data-stu-id="4cc22-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="4cc22-114">El intervalo de valores válidos es de 0 a D3D12 \_ req \_ subsources.</span><span class="sxs-lookup"><span data-stu-id="4cc22-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="4cc22-115">*NumSubresources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4cc22-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc22-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc22-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cc22-117">El número de Subrecursos del recurso.</span><span class="sxs-lookup"><span data-stu-id="4cc22-117">The number of subresources in the resource.</span></span> <span data-ttu-id="4cc22-118">El intervalo de valores válidos es de 0 a (D3D12 \_ req \_ subsources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="4cc22-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc22-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cc22-119">Return value</span></span>

<span data-ttu-id="4cc22-120">Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc22-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4cc22-121">Tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4cc22-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc22-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cc22-122">Requirements</span></span>



| <span data-ttu-id="4cc22-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cc22-123">Requirement</span></span> | <span data-ttu-id="4cc22-124">Value</span><span class="sxs-lookup"><span data-stu-id="4cc22-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc22-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cc22-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc22-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc22-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4cc22-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cc22-127">Library</span></span><br/> | <dl> <span data-ttu-id="4cc22-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cc22-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4cc22-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4cc22-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="4cc22-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cc22-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc22-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cc22-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc22-132">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4cc22-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

