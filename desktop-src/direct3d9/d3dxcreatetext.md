---
description: Crea una malla que contiene el texto especificado, usando la fuente asociada al contexto del dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Función D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698262"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="1a918-103">D3DXCreateText función)</span><span class="sxs-lookup"><span data-stu-id="1a918-103">D3DXCreateText function</span></span>

<span data-ttu-id="1a918-104">Crea una malla que contiene el texto especificado, usando la fuente asociada al contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a918-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a918-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a918-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="1a918-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a918-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a918-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a918-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1a918-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1a918-109">Puntero al dispositivo que creó la malla.</span><span class="sxs-lookup"><span data-stu-id="1a918-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-110">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a918-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-111">Tipo: **HDC**</span><span class="sxs-lookup"><span data-stu-id="1a918-111">Type: **HDC**</span></span>

<span data-ttu-id="1a918-112">Contexto de dispositivo que contiene la fuente para la salida.</span><span class="sxs-lookup"><span data-stu-id="1a918-112">Device context, containing the font for output.</span></span> <span data-ttu-id="1a918-113">La fuente seleccionada por el contexto de dispositivo debe ser una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1a918-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-114">*pText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a918-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a918-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a918-116">Puntero a una cadena que especifica el texto que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="1a918-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="1a918-117">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1a918-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1a918-118">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1a918-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="1a918-119">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1a918-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-120">*Desviación* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a918-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a918-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a918-122">Desviación de la cuerda máxima de los contornos de fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1a918-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-123">*Extrusión* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a918-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a918-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a918-125">Cantidad para extruir el texto en la dirección z negativa.</span><span class="sxs-lookup"><span data-stu-id="1a918-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-126">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1a918-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a918-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1a918-128">Puntero a la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="1a918-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-129">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1a918-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a918-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1a918-131">Puntero a un búfer que contiene información de adyacencias.</span><span class="sxs-lookup"><span data-stu-id="1a918-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="1a918-132">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1a918-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1a918-133">*pGlyphMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1a918-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a918-134">Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="1a918-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="1a918-135">Puntero a una matriz de estructuras [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) que contienen los datos de métricas del glifo.</span><span class="sxs-lookup"><span data-stu-id="1a918-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="1a918-136">Cada elemento contiene información sobre la posición y la orientación del glifo correspondiente en la cadena.</span><span class="sxs-lookup"><span data-stu-id="1a918-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="1a918-137">El número de elementos de la matriz debe ser igual al número de caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="1a918-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="1a918-138">Tenga en cuenta que el origen de cada estructura no es relativo a la cadena completa, sino que es relativo a esa celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="1a918-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="1a918-139">Para calcular el rectángulo de selección completo, agregue el incremento de cada glifo al atravesar la cadena.</span><span class="sxs-lookup"><span data-stu-id="1a918-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="1a918-140">Si no le preocupa los tamaños de glifo, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="1a918-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a918-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a918-141">Return value</span></span>

<span data-ttu-id="1a918-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a918-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a918-143">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a918-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1a918-144">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1a918-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a918-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a918-145">Remarks</span></span>

<span data-ttu-id="1a918-146">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="1a918-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1a918-147">Si se define Unicode, la llamada de función se resuelve como D3DXCreateTextW.</span><span class="sxs-lookup"><span data-stu-id="1a918-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="1a918-148">De lo contrario, la llamada de función se resuelve como D3DXCreateTextA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="1a918-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="1a918-149">Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).</span><span class="sxs-lookup"><span data-stu-id="1a918-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a918-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a918-150">Requirements</span></span>



| <span data-ttu-id="1a918-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a918-151">Requirement</span></span> | <span data-ttu-id="1a918-152">Value</span><span class="sxs-lookup"><span data-stu-id="1a918-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a918-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a918-153">Header</span></span><br/>  | <dl> <span data-ttu-id="1a918-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a918-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="1a918-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a918-155">Library</span></span><br/> | <dl> <span data-ttu-id="1a918-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a918-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1a918-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a918-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a918-158">Funciones de dibujo de forma</span><span class="sxs-lookup"><span data-stu-id="1a918-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
