---
description: Recupera información acerca de una imagen determinada en un recurso.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Función D3DXGetImageInfoFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821079"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="6873a-103">D3DXGetImageInfoFromResource función)</span><span class="sxs-lookup"><span data-stu-id="6873a-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="6873a-104">Recupera información acerca de una imagen determinada en un recurso.</span><span class="sxs-lookup"><span data-stu-id="6873a-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="6873a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6873a-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6873a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6873a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6873a-107">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6873a-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6873a-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6873a-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6873a-109">Módulo en el que se carga el recurso.</span><span class="sxs-lookup"><span data-stu-id="6873a-109">Module where the resource is loaded.</span></span> <span data-ttu-id="6873a-110">Establezca este parámetro en **null** para especificar el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="6873a-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="6873a-111">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6873a-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6873a-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6873a-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6873a-113">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6873a-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="6873a-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6873a-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6873a-115">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6873a-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6873a-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6873a-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6873a-117">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6873a-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6873a-118">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6873a-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6873a-119">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6873a-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6873a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6873a-120">Return value</span></span>

<span data-ttu-id="6873a-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6873a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6873a-122">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6873a-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6873a-123">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6873a-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6873a-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6873a-124">Remarks</span></span>

<span data-ttu-id="6873a-125">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="6873a-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6873a-126">Si se define Unicode, la llamada de función se resuelve como D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="6873a-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="6873a-127">De lo contrario, la llamada de función se resuelve como D3DXGetImageInfoFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="6873a-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6873a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6873a-128">Requirements</span></span>



| <span data-ttu-id="6873a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6873a-129">Requirement</span></span> | <span data-ttu-id="6873a-130">Value</span><span class="sxs-lookup"><span data-stu-id="6873a-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6873a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6873a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6873a-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6873a-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6873a-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6873a-133">Library</span></span><br/> | <dl> <span data-ttu-id="6873a-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6873a-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6873a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6873a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6873a-136">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6873a-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6873a-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="6873a-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="6873a-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6873a-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
