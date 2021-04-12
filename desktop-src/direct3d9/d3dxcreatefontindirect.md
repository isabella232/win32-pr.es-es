---
description: Crea un objeto de fuente indirectamente para un dispositivo y una fuente.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Función D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362691"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="4a9aa-103">D3DXCreateFontIndirect función)</span><span class="sxs-lookup"><span data-stu-id="4a9aa-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="4a9aa-104">Crea un objeto de fuente indirectamente para un dispositivo y una fuente.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a9aa-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="4a9aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a9aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a9aa-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a9aa-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9aa-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4a9aa-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4a9aa-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el dispositivo que se va a asociar al objeto de fuente.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="4a9aa-110">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a9aa-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9aa-111">Tipo: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a9aa-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="4a9aa-112">Puntero a una [**estructura \_ DESC de D3DXFONT**](d3dxfont-desc.md) , que describe los atributos del objeto de fuente que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="4a9aa-113">Si la configuración del compilador requiere Unicode, el tipo de datos D3DXFONT \_ desc se resuelve como D3DXFONT \_ DESCW; de lo contrario, el tipo de datos se resuelve como D3DXFONT \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="4a9aa-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4a9aa-115">*ppFont* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a9aa-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9aa-116">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a9aa-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="4a9aa-117">Devuelve un puntero a una interfaz [**ID3DXFont**](id3dxfont.md) que representa el objeto de fuente creado.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a9aa-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a9aa-118">Return value</span></span>

<span data-ttu-id="4a9aa-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a9aa-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a9aa-120">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a9aa-121">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a9aa-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a9aa-122">Remarks</span></span>

<span data-ttu-id="4a9aa-123">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4a9aa-124">Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="4a9aa-125">De lo contrario, la llamada de función se resuelve como D3DXCreateFontIndirectA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="4a9aa-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a9aa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a9aa-126">Requirements</span></span>



| <span data-ttu-id="4a9aa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a9aa-127">Requirement</span></span> | <span data-ttu-id="4a9aa-128">Value</span><span class="sxs-lookup"><span data-stu-id="4a9aa-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9aa-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a9aa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4a9aa-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a9aa-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4a9aa-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a9aa-131">Library</span></span><br/> | <dl> <span data-ttu-id="4a9aa-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a9aa-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a9aa-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a9aa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9aa-134">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="4a9aa-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
