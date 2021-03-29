---
title: Función D3DX11CreateThreadPump (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un bombeo de subprocesos.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Función D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987012"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="b1b53-106">D3DX11CreateThreadPump función)</span><span class="sxs-lookup"><span data-stu-id="b1b53-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="b1b53-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="b1b53-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="b1b53-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b1b53-108">See Remarks.</span></span>

 

<span data-ttu-id="b1b53-109">Cree un bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b1b53-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b53-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1b53-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="b1b53-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1b53-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b53-112">*cIoThreads* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1b53-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b53-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1b53-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1b53-114">Número de subprocesos de e/s que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="b1b53-114">The number of I/O threads to create.</span></span> <span data-ttu-id="b1b53-115">Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="b1b53-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b1b53-116">*cProcThreads* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1b53-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b53-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1b53-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1b53-118">Número de subprocesos del proceso que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="b1b53-118">The number of process threads to create.</span></span> <span data-ttu-id="b1b53-119">Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="b1b53-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b1b53-120">*ppThreadPump* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b1b53-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b53-121">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1b53-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="b1b53-122">El bombeo de subprocesos creado.</span><span class="sxs-lookup"><span data-stu-id="b1b53-122">The created thread pump.</span></span> <span data-ttu-id="b1b53-123">Consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b1b53-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b53-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1b53-124">Return value</span></span>

<span data-ttu-id="b1b53-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1b53-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1b53-126">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b1b53-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b53-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1b53-127">Remarks</span></span>

<span data-ttu-id="b1b53-128">Un bombeo de subprocesos es un objeto que consume muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="b1b53-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="b1b53-129">Solo se debe crear un bombeo de subprocesos por aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1b53-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="b1b53-130">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="b1b53-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="b1b53-131">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="b1b53-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="b1b53-132">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b1b53-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b53-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1b53-133">Requirements</span></span>



| <span data-ttu-id="b1b53-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b53-134">Requirement</span></span> | <span data-ttu-id="b1b53-135">Value</span><span class="sxs-lookup"><span data-stu-id="b1b53-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b53-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1b53-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b1b53-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b53-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="b1b53-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1b53-138">Library</span></span><br/> | <dl> <span data-ttu-id="b1b53-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1b53-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1b53-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1b53-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b53-141">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="b1b53-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

