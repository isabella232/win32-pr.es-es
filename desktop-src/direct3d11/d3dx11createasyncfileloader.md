---
title: Función D3DX11CreateAsyncFileLoader (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un cargador de archivos asincrónicos.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- Función D3DX11CreateAsyncFileLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637b2eddb035d937315582188295d93d9fd0e9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998557"
---
# <a name="d3dx11createasyncfileloader-function"></a><span data-ttu-id="93816-106">D3DX11CreateAsyncFileLoader función)</span><span class="sxs-lookup"><span data-stu-id="93816-106">D3DX11CreateAsyncFileLoader function</span></span>

> [!Note]  
> <span data-ttu-id="93816-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="93816-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="93816-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="93816-108">See Remarks.</span></span>

 

<span data-ttu-id="93816-109">Cree un cargador de archivos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="93816-109">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="93816-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93816-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="93816-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93816-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93816-112">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93816-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93816-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="93816-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="93816-114">Nombre del archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="93816-114">The name of the file to load.</span></span> <span data-ttu-id="93816-115">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="93816-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="93816-116">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="93816-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="93816-117">*ppDataLoader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="93816-117">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93816-118">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="93816-118">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="93816-119">Dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX11DataLoader (interfaz**](id3dx11dataloader.md))).</span><span class="sxs-lookup"><span data-stu-id="93816-119">Address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93816-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93816-120">Return value</span></span>

<span data-ttu-id="93816-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93816-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93816-122">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="93816-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93816-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93816-123">Remarks</span></span>

<span data-ttu-id="93816-124">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="93816-124">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="93816-125">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="93816-125">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="93816-126">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="93816-126">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="93816-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93816-127">Requirements</span></span>



| <span data-ttu-id="93816-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="93816-128">Requirement</span></span> | <span data-ttu-id="93816-129">Value</span><span class="sxs-lookup"><span data-stu-id="93816-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93816-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93816-130">Header</span></span><br/>  | <dl> <span data-ttu-id="93816-131"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="93816-131"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="93816-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93816-132">Library</span></span><br/> | <dl> <span data-ttu-id="93816-133"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93816-133"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="93816-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="93816-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93816-135">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="93816-135">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

