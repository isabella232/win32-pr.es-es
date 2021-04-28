---
description: 'Función D3DXGetImageInfoFromFile: recupera información sobre un archivo de imagen determinado.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Función D3DXGetImageInfoFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114503"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="6442c-103">Función D3DXGetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="6442c-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="6442c-104">Recupera información sobre un archivo de imagen determinado.</span><span class="sxs-lookup"><span data-stu-id="6442c-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6442c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6442c-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6442c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6442c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6442c-107">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6442c-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6442c-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6442c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6442c-109">Nombre de archivo de la imagen sobre la que recuperar información.</span><span class="sxs-lookup"><span data-stu-id="6442c-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="6442c-110">Si se definen \_ UNICODE o UNICODE, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6442c-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6442c-111">*pSrcInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6442c-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6442c-112">Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6442c-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6442c-113">Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se rellenará con la descripción de los datos del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="6442c-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6442c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6442c-114">Return value</span></span>

<span data-ttu-id="6442c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6442c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6442c-116">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6442c-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6442c-117">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6442c-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6442c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6442c-118">Remarks</span></span>

<span data-ttu-id="6442c-119">Esta función admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="6442c-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="6442c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6442c-120">Requirements</span></span>



| <span data-ttu-id="6442c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6442c-121">Requirement</span></span> | <span data-ttu-id="6442c-122">Value</span><span class="sxs-lookup"><span data-stu-id="6442c-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6442c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6442c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6442c-124"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="6442c-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6442c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6442c-125">Library</span></span><br/> | <dl> <span data-ttu-id="6442c-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6442c-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6442c-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6442c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6442c-128">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6442c-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6442c-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6442c-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6442c-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="6442c-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
