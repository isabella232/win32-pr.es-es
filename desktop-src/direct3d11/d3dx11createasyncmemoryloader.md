---
title: Función D3DX11CreateAsyncMemoryLoader (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un cargador de memoria asincrónica.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- Función D3DX11CreateAsyncMemoryLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998550"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="8cc44-106">D3DX11CreateAsyncMemoryLoader función)</span><span class="sxs-lookup"><span data-stu-id="8cc44-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="8cc44-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8cc44-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="8cc44-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8cc44-108">See Remarks.</span></span>

 

<span data-ttu-id="8cc44-109">Cree un cargador de memoria asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8cc44-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc44-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cc44-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="8cc44-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cc44-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc44-112">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cc44-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc44-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8cc44-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8cc44-114">Puntero en los datos.</span><span class="sxs-lookup"><span data-stu-id="8cc44-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="8cc44-115">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cc44-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc44-116">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8cc44-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8cc44-117">Tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="8cc44-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="8cc44-118">*ppDataLoader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8cc44-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc44-119">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8cc44-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="8cc44-120">La dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX11DataLoader (interfaz**](id3dx11dataloader.md))).</span><span class="sxs-lookup"><span data-stu-id="8cc44-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc44-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cc44-121">Return value</span></span>

<span data-ttu-id="8cc44-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cc44-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cc44-123">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8cc44-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc44-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cc44-124">Remarks</span></span>

<span data-ttu-id="8cc44-125">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="8cc44-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="8cc44-126">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="8cc44-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="8cc44-127">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8cc44-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc44-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc44-128">Requirements</span></span>



| <span data-ttu-id="8cc44-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc44-129">Requirement</span></span> | <span data-ttu-id="8cc44-130">Value</span><span class="sxs-lookup"><span data-stu-id="8cc44-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc44-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cc44-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc44-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc44-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="8cc44-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cc44-133">Library</span></span><br/> | <dl> <span data-ttu-id="8cc44-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cc44-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8cc44-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cc44-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc44-136">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="8cc44-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

