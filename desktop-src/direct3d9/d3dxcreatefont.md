---
description: Crea un objeto de fuente para un dispositivo y fuente.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Función D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821279"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="81710-103">D3DXCreateFont función)</span><span class="sxs-lookup"><span data-stu-id="81710-103">D3DXCreateFont function</span></span>

<span data-ttu-id="81710-104">Crea un objeto de fuente para un dispositivo y fuente.</span><span class="sxs-lookup"><span data-stu-id="81710-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="81710-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81710-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="81710-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81710-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="81710-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="81710-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="81710-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="81710-110">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="81710-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-112">Alto de los caracteres en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="81710-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="81710-113">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="81710-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-115">Ancho de los caracteres de las unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="81710-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="81710-116">*Peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="81710-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-118">Peso del tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="81710-118">Typeface weight.</span></span> <span data-ttu-id="81710-119">Un ejemplo está en negrita.</span><span class="sxs-lookup"><span data-stu-id="81710-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="81710-120">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-122">Número de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="81710-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="81710-123">*Cursiva* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-124">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-125">True para la fuente cursiva; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="81710-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="81710-126">*Juego de caracteres* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-128">Juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="81710-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="81710-129">*OutputPrecision* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-131">Especifica el modo en que Windows debe intentar hacer coincidir los tamaños de fuente y las características deseadas con las fuentes reales.</span><span class="sxs-lookup"><span data-stu-id="81710-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="81710-132">Use \_ solo TT \_ \_ PRECIS por ejemplo para asegurarse de que siempre obtiene una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="81710-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="81710-133">*Calidad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="81710-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-135">Especifica el modo en que Windows debe coincidir con la fuente deseada con una fuente real.</span><span class="sxs-lookup"><span data-stu-id="81710-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="81710-136">Solo se aplica a las fuentes de trama y no debe afectar a las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="81710-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="81710-137">*PitchAndFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-139">Índice de paso y familia.</span><span class="sxs-lookup"><span data-stu-id="81710-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="81710-140">*pFacename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81710-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-141">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81710-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81710-142">Cadena que contiene el nombre del tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="81710-142">String containing the typeface name.</span></span> <span data-ttu-id="81710-143">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="81710-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="81710-144">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="81710-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="81710-145">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="81710-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81710-146">*ppFont* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="81710-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81710-147">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="81710-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="81710-148">Devuelve un puntero a una interfaz [**ID3DXFont**](id3dxfont.md) que representa el objeto de fuente creado.</span><span class="sxs-lookup"><span data-stu-id="81710-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81710-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81710-149">Return value</span></span>

<span data-ttu-id="81710-150">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81710-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81710-151">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81710-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81710-152">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="81710-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="81710-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81710-153">Remarks</span></span>

<span data-ttu-id="81710-154">La creación de un objeto ID3DXFont requiere que el dispositivo admita el color de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="81710-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="81710-155">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="81710-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="81710-156">Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="81710-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="81710-157">De lo contrario, la llamada de función se resuelve como D3DXCreateFontA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="81710-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="81710-158">Si desea obtener más información sobre los parámetros de fuente, consulte [la fuente lógica](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="81710-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81710-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81710-159">Requirements</span></span>



| <span data-ttu-id="81710-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="81710-160">Requirement</span></span> | <span data-ttu-id="81710-161">Value</span><span class="sxs-lookup"><span data-stu-id="81710-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81710-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81710-162">Header</span></span><br/>  | <dl> <span data-ttu-id="81710-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="81710-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="81710-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81710-164">Library</span></span><br/> | <dl> <span data-ttu-id="81710-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81710-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81710-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="81710-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81710-167">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="81710-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
