---
title: Función D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un procesador de datos para usarlo con un bombeo de subprocesos. | Función D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Función D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998544"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="8d97e-107">D3DX11CreateAsyncTextureInfoProcessor función)</span><span class="sxs-lookup"><span data-stu-id="8d97e-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="8d97e-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8d97e-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="8d97e-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8d97e-109">See Remarks.</span></span>

 

<span data-ttu-id="8d97e-110">Cree un procesador de datos para usarlo con un [**bombeo de subprocesos**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="8d97e-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d97e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d97e-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="8d97e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d97e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d97e-113">*pImageInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d97e-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d97e-114">Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d97e-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="8d97e-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8d97e-115">Optional.</span></span> <span data-ttu-id="8d97e-116">Identifica las características de una textura (consulte [**\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="8d97e-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8d97e-117">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d97e-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d97e-118">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8d97e-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="8d97e-119">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="8d97e-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d97e-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d97e-120">Return value</span></span>

<span data-ttu-id="8d97e-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d97e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d97e-122">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8d97e-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d97e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d97e-123">Remarks</span></span>

<span data-ttu-id="8d97e-124">Esta API crea una interfaz de procesador de datos; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) crea la interfaz del procesador de datos y carga la textura.</span><span class="sxs-lookup"><span data-stu-id="8d97e-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="8d97e-125">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="8d97e-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="8d97e-126">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="8d97e-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="8d97e-127">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8d97e-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d97e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d97e-128">Requirements</span></span>



| <span data-ttu-id="8d97e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d97e-129">Requirement</span></span> | <span data-ttu-id="8d97e-130">Value</span><span class="sxs-lookup"><span data-stu-id="8d97e-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d97e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d97e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8d97e-132"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d97e-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8d97e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d97e-133">Library</span></span><br/> | <dl> <span data-ttu-id="8d97e-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d97e-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8d97e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d97e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d97e-136">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="8d97e-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

