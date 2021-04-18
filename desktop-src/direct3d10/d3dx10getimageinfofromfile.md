---
description: Recupera información sobre un archivo de imagen determinado.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: Función D3DX10GetImageInfoFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 836d2e18b5c1c48bbe64d0026e97f8ebc5a066ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707728"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="a30a5-103">D3DX10GetImageInfoFromFile función)</span><span class="sxs-lookup"><span data-stu-id="a30a5-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="a30a5-104">Recupera información sobre un archivo de imagen determinado.</span><span class="sxs-lookup"><span data-stu-id="a30a5-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a30a5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a30a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a30a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30a5-107">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30a5-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30a5-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a30a5-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a30a5-109">Nombre de archivo de la imagen sobre la que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="a30a5-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="a30a5-110">Si se definen Unicode o \_ Unicode, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a30a5-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a30a5-111">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30a5-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30a5-112">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a30a5-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a30a5-113">Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a30a5-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="a30a5-114">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a30a5-114">Can be **NULL**.</span></span> <span data-ttu-id="a30a5-115">Vea [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a30a5-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="a30a5-116">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30a5-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30a5-117">Tipo: **[ **\_ \_ información de imagen de D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a30a5-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="a30a5-118">Puntero a una \_ estructura de \_ información de imagen D3DX10 que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a30a5-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="a30a5-119">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a30a5-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a30a5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a30a5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a30a5-121">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a30a5-121">A pointer to the return value.</span></span> <span data-ttu-id="a30a5-122">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a30a5-122">May be **NULL**.</span></span> <span data-ttu-id="a30a5-123">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a30a5-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30a5-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30a5-124">Return value</span></span>

<span data-ttu-id="a30a5-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a30a5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a30a5-126">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a30a5-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a30a5-127">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="a30a5-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a30a5-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a30a5-128">Remarks</span></span>

<span data-ttu-id="a30a5-129">Esta función admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="a30a5-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30a5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30a5-130">Requirements</span></span>



| <span data-ttu-id="a30a5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30a5-131">Requirement</span></span> | <span data-ttu-id="a30a5-132">Value</span><span class="sxs-lookup"><span data-stu-id="a30a5-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a30a5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a30a5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a30a5-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a30a5-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a30a5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a30a5-135">Library</span></span><br/> | <dl> <span data-ttu-id="a30a5-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a30a5-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a30a5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a30a5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30a5-138">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="a30a5-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
