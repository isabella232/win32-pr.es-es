---
title: Función D3D12GetFormatPlaneCount (D3dx12. h)
description: Obtiene el número de planos para el formato de DXGI especificado para el adaptador virtual especificado (un ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount función)
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707757"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="2b3e3-104">D3D12GetFormatPlaneCount función)</span><span class="sxs-lookup"><span data-stu-id="2b3e3-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="2b3e3-105">Obtiene el número de planos para el formato de DXGI especificado para el adaptador virtual especificado (un **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="2b3e3-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3e3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b3e3-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="2b3e3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b3e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b3e3-108">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b3e3-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b3e3-109">Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="2b3e3-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="2b3e3-110">Adaptador virtual (un [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) para el que se va a obtener el número de planos.</span><span class="sxs-lookup"><span data-stu-id="2b3e3-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="2b3e3-111">*Format*</span><span class="sxs-lookup"><span data-stu-id="2b3e3-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="2b3e3-112">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2b3e3-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2b3e3-113">El [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) para el que se va a obtener el número de planos.</span><span class="sxs-lookup"><span data-stu-id="2b3e3-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b3e3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b3e3-114">Return value</span></span>

<span data-ttu-id="2b3e3-115">Tipo: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="2b3e3-115">Type: **UINT8**</span></span>

<span data-ttu-id="2b3e3-116">Recuento de planos para el formato especificado en el adaptador virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="2b3e3-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b3e3-117">Requirements</span></span>



| <span data-ttu-id="2b3e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b3e3-118">Requirement</span></span> | <span data-ttu-id="2b3e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="2b3e3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3e3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b3e3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2b3e3-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e3-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2b3e3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b3e3-122">Library</span></span><br/> | <dl> <span data-ttu-id="2b3e3-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e3-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b3e3-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b3e3-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b3e3-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e3-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b3e3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b3e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3e3-127">**\_Información de \_ formato de datos de características de D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b3e3-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="2b3e3-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="2b3e3-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="2b3e3-129">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="2b3e3-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

