---
description: Crea un objeto de fuente para un dispositivo y fuente. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar DirectWrite y la biblioteca DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Función D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707944"
---
# <a name="d3dx10createfont-function"></a><span data-ttu-id="808e3-103">D3DX10CreateFont función)</span><span class="sxs-lookup"><span data-stu-id="808e3-103">D3DX10CreateFont function</span></span>

<span data-ttu-id="808e3-104">Crea un objeto de fuente para un dispositivo y fuente.</span><span class="sxs-lookup"><span data-stu-id="808e3-104">Creates a font object for a device and font.</span></span>

> [!Note]  
> <span data-ttu-id="808e3-105">En lugar de usar esta función, se recomienda usar [DirectWrite](../directwrite/direct-write-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.</span><span class="sxs-lookup"><span data-stu-id="808e3-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="808e3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="808e3-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="808e3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="808e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="808e3-108">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="808e3-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="808e3-110">Puntero a una interfaz ID3D10Device, el dispositivo que se va a asociar al objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="808e3-110">Pointer to an ID3D10Device interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-111">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-111">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-113">Alto de los caracteres en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="808e3-113">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-114">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-116">Ancho de los caracteres de las unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="808e3-116">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-117">*Peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-117">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-119">Peso del tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="808e3-119">Typeface weight.</span></span> <span data-ttu-id="808e3-120">Un ejemplo está en negrita.</span><span class="sxs-lookup"><span data-stu-id="808e3-120">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-121">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-121">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-123">Número de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="808e3-123">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-124">*Cursiva* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-124">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-125">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-125">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-126">True para la fuente cursiva; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="808e3-126">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-127">*Juego de caracteres* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-127">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-129">Juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="808e3-129">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-130">*OutputPrecision* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-130">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-131">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-132">Especifica el modo en que Windows debe intentar hacer coincidir los tamaños de fuente y las características deseadas con las fuentes reales.</span><span class="sxs-lookup"><span data-stu-id="808e3-132">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="808e3-133">Use \_ solo TT \_ \_ PRECIS por ejemplo para asegurarse de que siempre obtiene una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="808e3-133">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-134">*Calidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-134">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-136">Especifica el modo en que Windows debe coincidir con la fuente deseada con una fuente real.</span><span class="sxs-lookup"><span data-stu-id="808e3-136">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="808e3-137">Solo se aplica a las fuentes de trama y no debe afectar a las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="808e3-137">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-138">*PitchAndFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-138">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-139">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-139">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-140">Índice de paso y familia.</span><span class="sxs-lookup"><span data-stu-id="808e3-140">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-141">*pFaceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="808e3-141">*pFaceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-142">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808e3-142">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808e3-143">Cadena que contiene el nombre del tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="808e3-143">String containing the typeface name.</span></span> <span data-ttu-id="808e3-144">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="808e3-144">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="808e3-145">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="808e3-145">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="808e3-146">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="808e3-146">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="808e3-147">*ppFont* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="808e3-147">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="808e3-148">Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="808e3-148">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="808e3-149">Devuelve un puntero a una interfaz ID3DX10Font que representa el objeto de fuente creado.</span><span class="sxs-lookup"><span data-stu-id="808e3-149">Returns a pointer to an ID3DX10Font interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="808e3-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="808e3-150">Return value</span></span>

<span data-ttu-id="808e3-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="808e3-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="808e3-152">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="808e3-152">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="808e3-153">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="808e3-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="808e3-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="808e3-154">Remarks</span></span>

<span data-ttu-id="808e3-155">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="808e3-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="808e3-156">Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="808e3-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="808e3-157">De lo contrario, la llamada de función se resuelve como D3DXCreateFontA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="808e3-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="808e3-158">Si desea obtener más información sobre los parámetros de fuente, consulte [la fuente lógica](/previous-versions//ms533985(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="808e3-158">If you want more information about font parameters, see [The Logical Font](/previous-versions//ms533985(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="808e3-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="808e3-159">Requirements</span></span>



| <span data-ttu-id="808e3-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="808e3-160">Requirement</span></span> | <span data-ttu-id="808e3-161">Value</span><span class="sxs-lookup"><span data-stu-id="808e3-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="808e3-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="808e3-162">Header</span></span><br/>  | <dl> <span data-ttu-id="808e3-163"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="808e3-163"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="808e3-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="808e3-164">Library</span></span><br/> | <dl> <span data-ttu-id="808e3-165"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="808e3-165"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="808e3-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="808e3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808e3-167">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="808e3-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
