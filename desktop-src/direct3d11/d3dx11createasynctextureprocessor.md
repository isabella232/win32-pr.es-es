---
title: Función D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un procesador de datos para usarlo con un bombeo de subprocesos. | Función D3DX11CreateAsyncTextureProcessor (D3DX11tex. h)
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- Función D3DX11CreateAsyncTextureProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998532"
---
# <a name="d3dx11createasynctextureprocessor-function"></a><span data-ttu-id="6b97d-107">D3DX11CreateAsyncTextureProcessor función)</span><span class="sxs-lookup"><span data-stu-id="6b97d-107">D3DX11CreateAsyncTextureProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="6b97d-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="6b97d-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="6b97d-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6b97d-109">See Remarks.</span></span>

 

<span data-ttu-id="6b97d-110">Cree un procesador de datos para usarlo con un [**bombeo de subprocesos**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="6b97d-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b97d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b97d-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="6b97d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b97d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b97d-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b97d-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b97d-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="6b97d-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="6b97d-115">Un puntero a devive (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span><span class="sxs-lookup"><span data-stu-id="6b97d-115">A pointer to the devive (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span></span>

</dd> <dt>

<span data-ttu-id="6b97d-116">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b97d-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b97d-117">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b97d-117">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="6b97d-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6b97d-118">Optional.</span></span> <span data-ttu-id="6b97d-119">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="6b97d-119">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="6b97d-120">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6b97d-120">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b97d-121">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b97d-121">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="6b97d-122">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="6b97d-122">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b97d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b97d-123">Return value</span></span>

<span data-ttu-id="6b97d-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b97d-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b97d-125">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6b97d-125">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b97d-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b97d-126">Remarks</span></span>

<span data-ttu-id="6b97d-127">Esta API crea una interfaz de procesador de datos y carga la textura; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) crea la interfaz del procesador de datos.</span><span class="sxs-lookup"><span data-stu-id="6b97d-127">This API does creates a data-processor interface and loads the texture; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

<span data-ttu-id="6b97d-128">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="6b97d-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="6b97d-129">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="6b97d-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="6b97d-130">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6b97d-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b97d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b97d-131">Requirements</span></span>



| <span data-ttu-id="6b97d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b97d-132">Requirement</span></span> | <span data-ttu-id="6b97d-133">Value</span><span class="sxs-lookup"><span data-stu-id="6b97d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b97d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b97d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="6b97d-135"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b97d-135"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6b97d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b97d-136">Library</span></span><br/> | <dl> <span data-ttu-id="6b97d-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b97d-137"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6b97d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b97d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b97d-139">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="6b97d-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

