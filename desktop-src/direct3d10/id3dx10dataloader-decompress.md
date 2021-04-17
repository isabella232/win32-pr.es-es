---
description: Se usa para descomprimir datos codificados. Normalmente, esto se utilizaría para cargar recursos desde sistemas de archivos, como archivos ZIP. Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader::D método ecompress (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698267"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="b5d69-105">ID3DX10DataLoader::D método ecompress</span><span class="sxs-lookup"><span data-stu-id="b5d69-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="b5d69-106">Se usa para descomprimir datos codificados.</span><span class="sxs-lookup"><span data-stu-id="b5d69-106">Used to decompress encoded data.</span></span> <span data-ttu-id="b5d69-107">Normalmente, esto se utilizaría para cargar recursos desde sistemas de archivos, como archivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="b5d69-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="b5d69-108">Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="b5d69-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d69-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5d69-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="b5d69-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5d69-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d69-111">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5d69-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d69-112">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="b5d69-112">Type: **void\*\***</span></span>

<span data-ttu-id="b5d69-113">Puntero a los datos sin procesar que se van a descomprimir.</span><span class="sxs-lookup"><span data-stu-id="b5d69-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="b5d69-114">*pcBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5d69-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d69-115">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5d69-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b5d69-116">Tamaño de los datos a los que apunta ppData.</span><span class="sxs-lookup"><span data-stu-id="b5d69-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d69-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5d69-117">Return value</span></span>

<span data-ttu-id="b5d69-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5d69-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5d69-119">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b5d69-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d69-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5d69-120">Remarks</span></span>

<span data-ttu-id="b5d69-121">La [**interfaz ID3DX10DataLoader**](id3dx10dataloader.md) se puede heredar y sus miembros se pueden redefinir.</span><span class="sxs-lookup"><span data-stu-id="b5d69-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="b5d69-122">La descompresión se puede redefinir para admitir sus propios formatos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="b5d69-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d69-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d69-123">Requirements</span></span>



| <span data-ttu-id="b5d69-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d69-124">Requirement</span></span> | <span data-ttu-id="b5d69-125">Value</span><span class="sxs-lookup"><span data-stu-id="b5d69-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d69-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5d69-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d69-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d69-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5d69-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5d69-128">Library</span></span><br/> | <dl> <span data-ttu-id="b5d69-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d69-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d69-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5d69-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d69-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="b5d69-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="b5d69-132">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b5d69-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
