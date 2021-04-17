---
title: Función D3DX12SerializeVersionedRootSignature (D3dx12. h)
description: Ayuda a habilitar las características de la firma raíz 1,1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para generar firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1,0 cuando no se admite la versión 1,1.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature función)
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707752"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="87047-105">D3DX12SerializeVersionedRootSignature función)</span><span class="sxs-lookup"><span data-stu-id="87047-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="87047-106">Ayuda a habilitar las características de la firma raíz 1,1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para generar firmas raíz.</span><span class="sxs-lookup"><span data-stu-id="87047-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="87047-107">Este método auxiliar reconstruye una firma raíz de la versión 1,0 cuando no se admite la versión 1,1.</span><span class="sxs-lookup"><span data-stu-id="87047-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="87047-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87047-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="87047-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87047-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87047-110">*pRootSignatureDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87047-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87047-111">Tipo: **const D3D12 de la \_ \_ \_ firma \_ \* raíz con versión**</span><span class="sxs-lookup"><span data-stu-id="87047-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="87047-112">Especifica una descripción de la [**\_ \_ \_ firma raíz \_ D3D12 con versión**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) que contiene una descripción de cualquier versión de una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="87047-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="87047-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="87047-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="87047-114">Tipo: **\_ versión de \_ firma \_ raíz de D3D**</span><span class="sxs-lookup"><span data-stu-id="87047-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="87047-115">Especifica la versión máxima admitida de la [**\_ \_ firma \_ raíz D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span><span class="sxs-lookup"><span data-stu-id="87047-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="87047-116">*ppBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="87047-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87047-117">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="87047-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="87047-118">Un puntero a un bloque de memoria que recibe un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que se puede utilizar para tener acceso a la firma raíz serializada.</span><span class="sxs-lookup"><span data-stu-id="87047-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="87047-119">*ppErrorBlob* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87047-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87047-120">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="87047-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="87047-121">Un puntero a un bloque de memoria que recibe un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que se puede usar para obtener acceso a los mensajes de error del serializador, o **null** si no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="87047-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87047-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87047-122">Return value</span></span>

<span data-ttu-id="87047-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87047-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87047-124">Devuelve **S \_ OK** si es correcto; de lo contrario, devuelve uno de los [códigos de retorno de Direct3D 12](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="87047-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87047-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87047-125">Remarks</span></span>

<span data-ttu-id="87047-126">Esta función se liberó para que coincida con la actualización de aniversario de Windows 10 (14393).</span><span class="sxs-lookup"><span data-stu-id="87047-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="87047-127">Con el fin de admitir versiones de Windows 10 anteriores a este, el uso de esta función requiere que se configure d3d12. lib para la *carga retrasada*.</span><span class="sxs-lookup"><span data-stu-id="87047-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="87047-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87047-128">Requirements</span></span>



| <span data-ttu-id="87047-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="87047-129">Requirement</span></span> | <span data-ttu-id="87047-130">Value</span><span class="sxs-lookup"><span data-stu-id="87047-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87047-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87047-131">Header</span></span><br/>  | <dl> <span data-ttu-id="87047-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="87047-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="87047-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87047-133">Library</span></span><br/> | <dl> <span data-ttu-id="87047-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87047-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="87047-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87047-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="87047-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87047-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87047-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="87047-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87047-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="87047-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="87047-139">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="87047-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

