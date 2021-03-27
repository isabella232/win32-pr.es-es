---
title: Función D3DX11CreateAsyncResourceLoader (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un cargador de recursos asíncronos.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- Función D3DX11CreateAsyncResourceLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083770"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="26abd-106">D3DX11CreateAsyncResourceLoader función)</span><span class="sxs-lookup"><span data-stu-id="26abd-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="26abd-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="26abd-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="26abd-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="26abd-108">See Remarks.</span></span>

 

<span data-ttu-id="26abd-109">Cree un cargador de recursos asíncronos.</span><span class="sxs-lookup"><span data-stu-id="26abd-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="26abd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26abd-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="26abd-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26abd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26abd-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26abd-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26abd-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26abd-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26abd-114">Identificador del módulo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26abd-114">Handle to the resource module.</span></span> <span data-ttu-id="26abd-115">Use la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obtener el identificador.</span><span class="sxs-lookup"><span data-stu-id="26abd-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="26abd-116">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26abd-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26abd-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26abd-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26abd-118">Nombre del recurso en hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="26abd-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="26abd-119">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="26abd-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="26abd-120">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="26abd-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="26abd-121">*ppDataLoader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="26abd-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26abd-122">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="26abd-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="26abd-123">La dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX11DataLoader (interfaz**](id3dx11dataloader.md))).</span><span class="sxs-lookup"><span data-stu-id="26abd-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26abd-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26abd-124">Return value</span></span>

<span data-ttu-id="26abd-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26abd-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26abd-126">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="26abd-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26abd-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26abd-127">Remarks</span></span>

<span data-ttu-id="26abd-128">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="26abd-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="26abd-129">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="26abd-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="26abd-130">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="26abd-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="26abd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26abd-131">Requirements</span></span>



| <span data-ttu-id="26abd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="26abd-132">Requirement</span></span> | <span data-ttu-id="26abd-133">Value</span><span class="sxs-lookup"><span data-stu-id="26abd-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26abd-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26abd-134">Header</span></span><br/>  | <dl> <span data-ttu-id="26abd-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="26abd-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="26abd-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26abd-136">Library</span></span><br/> | <dl> <span data-ttu-id="26abd-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26abd-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="26abd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="26abd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26abd-139">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="26abd-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

