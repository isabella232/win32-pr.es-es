---
description: Crea un archivo. x y guarda la jerarquía de malla y sus animaciones correspondientes.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Función D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698230"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="643f3-103">D3DXSaveMeshHierarchyToFile función)</span><span class="sxs-lookup"><span data-stu-id="643f3-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="643f3-104">Crea un archivo. x y guarda la jerarquía de malla y sus animaciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="643f3-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="643f3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="643f3-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="643f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="643f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643f3-107">*pFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="643f3-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643f3-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="643f3-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="643f3-109">Puntero a una cadena que especifica el nombre del archivo. x que identifica la malla guardada.</span><span class="sxs-lookup"><span data-stu-id="643f3-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="643f3-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="643f3-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="643f3-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="643f3-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="643f3-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="643f3-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="643f3-113">*XFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="643f3-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643f3-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="643f3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="643f3-115">Formato del archivo. x (texto o binario, comprimido o no).</span><span class="sxs-lookup"><span data-stu-id="643f3-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="643f3-116">Consulte D3DXF \_ FILEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="643f3-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="643f3-117">D3DXF \_ fileformat \_ Compressed se puede combinar (mediante un OR lógico) con las \_ marcas de texto D3DXF FILEFORMAT \_ binary o D3DXF \_ fileformat \_ para reducir el tamaño del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="643f3-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="643f3-118">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="643f3-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643f3-119">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="643f3-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="643f3-120">Nodo raíz de la jerarquía que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="643f3-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="643f3-121">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="643f3-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="643f3-122">*pAnimController* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="643f3-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643f3-123">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="643f3-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="643f3-124">Controlador de animación que tiene conjuntos de animaciones que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="643f3-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="643f3-125">Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="643f3-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="643f3-126">*pUserDataSaver* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="643f3-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643f3-127">Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="643f3-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="643f3-128">Interfaz proporcionada por la aplicación que permite guardar datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="643f3-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="643f3-129">Vea [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="643f3-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643f3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="643f3-130">Return value</span></span>

<span data-ttu-id="643f3-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="643f3-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="643f3-132">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="643f3-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="643f3-133">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="643f3-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="643f3-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="643f3-134">Remarks</span></span>

<span data-ttu-id="643f3-135">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="643f3-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="643f3-136">Si se define Unicode, la llamada de función se resuelve como D3DXSaveMeshHierarchyToFileW.</span><span class="sxs-lookup"><span data-stu-id="643f3-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="643f3-137">De lo contrario, la llamada de función se resuelve como D3DXSaveMeshHierarchyToFileA.</span><span class="sxs-lookup"><span data-stu-id="643f3-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="643f3-138">Esta función no guarda los conjuntos de animaciones comprimidos.</span><span class="sxs-lookup"><span data-stu-id="643f3-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="643f3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="643f3-139">Requirements</span></span>



| <span data-ttu-id="643f3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="643f3-140">Requirement</span></span> | <span data-ttu-id="643f3-141">Value</span><span class="sxs-lookup"><span data-stu-id="643f3-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="643f3-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="643f3-142">Header</span></span><br/>  | <dl> <span data-ttu-id="643f3-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="643f3-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="643f3-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="643f3-144">Library</span></span><br/> | <dl> <span data-ttu-id="643f3-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="643f3-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="643f3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="643f3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643f3-147">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="643f3-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="643f3-148">Referencia de archivo X</span><span class="sxs-lookup"><span data-stu-id="643f3-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
