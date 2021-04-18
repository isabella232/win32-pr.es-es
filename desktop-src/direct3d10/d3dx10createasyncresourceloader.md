---
description: Cree un cargador de recursos asíncronos.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: Función D3DX10CreateAsyncResourceLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707809"
---
# <a name="d3dx10createasyncresourceloader-function"></a><span data-ttu-id="d19fb-103">D3DX10CreateAsyncResourceLoader función)</span><span class="sxs-lookup"><span data-stu-id="d19fb-103">D3DX10CreateAsyncResourceLoader function</span></span>

<span data-ttu-id="d19fb-104">Cree un cargador de recursos asíncronos.</span><span class="sxs-lookup"><span data-stu-id="d19fb-104">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d19fb-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="d19fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d19fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19fb-107">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d19fb-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19fb-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d19fb-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d19fb-109">Identificador del módulo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d19fb-109">Handle to the resource module.</span></span> <span data-ttu-id="d19fb-110">Use la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obtener el identificador.</span><span class="sxs-lookup"><span data-stu-id="d19fb-110">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="d19fb-111">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d19fb-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19fb-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d19fb-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d19fb-113">Nombre del recurso en hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="d19fb-113">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="d19fb-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="d19fb-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d19fb-115">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d19fb-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d19fb-116">*ppDataLoader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d19fb-116">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d19fb-117">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d19fb-117">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="d19fb-118">La dirección de un puntero al procesador de datos asincrónicos (consulte la [**interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d19fb-118">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19fb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d19fb-119">Return value</span></span>

<span data-ttu-id="d19fb-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d19fb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d19fb-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d19fb-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d19fb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d19fb-122">Requirements</span></span>



| <span data-ttu-id="d19fb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d19fb-123">Requirement</span></span> | <span data-ttu-id="d19fb-124">Value</span><span class="sxs-lookup"><span data-stu-id="d19fb-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d19fb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d19fb-125">Header</span></span><br/> | <dl> <span data-ttu-id="d19fb-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d19fb-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d19fb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d19fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19fb-128">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="d19fb-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
