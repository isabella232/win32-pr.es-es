---
title: Función D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Función D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998538"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="caeef-104">D3DX11CreateAsyncShaderResourceViewProcessor función)</span><span class="sxs-lookup"><span data-stu-id="caeef-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="caeef-105">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="caeef-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="caeef-106">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="caeef-106">See Remarks.</span></span>

 

<span data-ttu-id="caeef-107">Cree un procesador de datos que cargue un recurso y, a continuación, cree una vista de recursos del sombreador para él.</span><span class="sxs-lookup"><span data-stu-id="caeef-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="caeef-108">Los procesadores de datos son un componente de la característica de carga asincrónica de datos de D3DX11 que usa los [**bombeos de subprocesos**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="caeef-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="caeef-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="caeef-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="caeef-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="caeef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caeef-111">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="caeef-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caeef-112">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="caeef-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="caeef-113">Puntero al dispositivo Direct3D (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que se usará para crear un recurso y una vista de recursos del sombreador para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="caeef-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="caeef-114">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="caeef-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caeef-115">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="caeef-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="caeef-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="caeef-116">Optional.</span></span> <span data-ttu-id="caeef-117">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="caeef-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="caeef-118">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="caeef-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="caeef-119">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="caeef-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="caeef-120">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="caeef-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caeef-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="caeef-121">Return value</span></span>

<span data-ttu-id="caeef-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="caeef-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="caeef-123">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="caeef-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="caeef-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="caeef-124">Remarks</span></span>

<span data-ttu-id="caeef-125">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="caeef-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="caeef-126">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="caeef-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="caeef-127">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="caeef-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="caeef-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caeef-128">Requirements</span></span>



| <span data-ttu-id="caeef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="caeef-129">Requirement</span></span> | <span data-ttu-id="caeef-130">Value</span><span class="sxs-lookup"><span data-stu-id="caeef-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="caeef-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="caeef-131">Header</span></span><br/>  | <dl> <span data-ttu-id="caeef-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="caeef-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="caeef-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="caeef-133">Library</span></span><br/> | <dl> <span data-ttu-id="caeef-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caeef-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="caeef-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="caeef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caeef-136">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="caeef-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

