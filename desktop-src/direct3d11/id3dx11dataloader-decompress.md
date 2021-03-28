---
title: Método Descomprimie ID3DX11DataLoader (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Descomprime los datos codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Descomprimir método Direct3D 11
- Método descomprimite Direct3D 11, interfaz ID3DX11DataLoader
- Interfaz ID3DX11DataLoader Direct3D 11, método Descomprimite
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003974"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="4e0c7-107">ID3DX11DataLoader::D método ecompress</span><span class="sxs-lookup"><span data-stu-id="4e0c7-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="4e0c7-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="4e0c7-109">Descomprime los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0c7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e0c7-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="4e0c7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e0c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0c7-112">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e0c7-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0c7-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="4e0c7-113">Type: **void\*\***</span></span>

<span data-ttu-id="4e0c7-114">Puntero a los datos sin procesar que se van a descomprimir.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="4e0c7-115">*pcBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e0c7-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0c7-116">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="4e0c7-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="4e0c7-117">Tamaño de los datos a los que apunta ppData.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e0c7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e0c7-118">Return value</span></span>

<span data-ttu-id="4e0c7-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e0c7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e0c7-120">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4e0c7-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e0c7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e0c7-121">Remarks</span></span>

<span data-ttu-id="4e0c7-122">Utilice este método para cargar recursos desde sistemas de archivos, como archivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="4e0c7-123">Al cargar desde un recurso sin comprimir, la fase de descompresión no tiene que realizar ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="4e0c7-124">La [**interfaz ID3DX11DataLoader**](id3dx11dataloader.md) se puede heredar y sus miembros se pueden redefinir para admitir formatos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="4e0c7-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0c7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e0c7-125">Requirements</span></span>



| <span data-ttu-id="4e0c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e0c7-126">Requirement</span></span> | <span data-ttu-id="4e0c7-127">Value</span><span class="sxs-lookup"><span data-stu-id="4e0c7-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0c7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e0c7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4e0c7-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0c7-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="4e0c7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e0c7-130">Library</span></span><br/> | <dl> <span data-ttu-id="4e0c7-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e0c7-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e0c7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e0c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0c7-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="4e0c7-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="4e0c7-134">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="4e0c7-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

