---
description: Recupera información sobre un archivo de imagen determinado.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Función D3DXGetImageInfoFromFile (D3dx9tex. h)
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
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718191"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="2b6f6-103">D3DXGetImageInfoFromFile función)</span><span class="sxs-lookup"><span data-stu-id="2b6f6-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="2b6f6-104">Recupera información sobre un archivo de imagen determinado.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b6f6-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2b6f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b6f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6f6-107">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b6f6-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6f6-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b6f6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b6f6-109">Nombre de archivo de la imagen sobre la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="2b6f6-110">Si se definen Unicode o \_ Unicode, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="2b6f6-111">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b6f6-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6f6-112">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b6f6-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2b6f6-113">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6f6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b6f6-114">Return value</span></span>

<span data-ttu-id="2b6f6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b6f6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b6f6-116">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b6f6-117">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="2b6f6-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6f6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b6f6-118">Remarks</span></span>

<span data-ttu-id="2b6f6-119">Esta función admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b6f6-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6f6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b6f6-120">Requirements</span></span>



| <span data-ttu-id="2b6f6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6f6-121">Requirement</span></span> | <span data-ttu-id="2b6f6-122">Value</span><span class="sxs-lookup"><span data-stu-id="2b6f6-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6f6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b6f6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2b6f6-124"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b6f6-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2b6f6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b6f6-125">Library</span></span><br/> | <dl> <span data-ttu-id="2b6f6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b6f6-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2b6f6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b6f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6f6-128">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2b6f6-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="2b6f6-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="2b6f6-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="2b6f6-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="2b6f6-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
