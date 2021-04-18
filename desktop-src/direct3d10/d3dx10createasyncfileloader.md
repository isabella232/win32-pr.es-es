---
description: Cree un cargador de archivos asincrónicos.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: Función D3DX10CreateAsyncFileLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717679"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="f34c8-103">D3DX10CreateAsyncFileLoader función)</span><span class="sxs-lookup"><span data-stu-id="f34c8-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="f34c8-104">Cree un cargador de archivos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="f34c8-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f34c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f34c8-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="f34c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f34c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f34c8-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f34c8-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f34c8-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f34c8-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f34c8-109">Nombre del archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="f34c8-109">The name of the file to load.</span></span> <span data-ttu-id="f34c8-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f34c8-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f34c8-111">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f34c8-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f34c8-112">*ppDataLoader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f34c8-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f34c8-113">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f34c8-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="f34c8-114">Dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX10DataLoader (interfaz**](id3dx10dataloader.md))).</span><span class="sxs-lookup"><span data-stu-id="f34c8-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f34c8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f34c8-115">Return value</span></span>

<span data-ttu-id="f34c8-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f34c8-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f34c8-117">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f34c8-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f34c8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f34c8-118">Requirements</span></span>



| <span data-ttu-id="f34c8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f34c8-119">Requirement</span></span> | <span data-ttu-id="f34c8-120">Value</span><span class="sxs-lookup"><span data-stu-id="f34c8-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34c8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f34c8-121">Header</span></span><br/> | <dl> <span data-ttu-id="f34c8-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="f34c8-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34c8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f34c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34c8-124">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="f34c8-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
