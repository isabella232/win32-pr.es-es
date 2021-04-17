---
description: Guarda una malla en un archivo. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Función D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698229"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="70943-103">D3DXSaveMeshToX función)</span><span class="sxs-lookup"><span data-stu-id="70943-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="70943-104">Guarda una malla en un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="70943-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="70943-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70943-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="70943-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70943-107">*pFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70943-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70943-109">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="70943-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="70943-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="70943-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="70943-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="70943-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="70943-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="70943-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="70943-113">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="70943-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="70943-115">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla que se va a guardar en un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="70943-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="70943-116">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="70943-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="70943-118">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="70943-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="70943-119">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="70943-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="70943-120">*pMaterials* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-121">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="70943-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="70943-122">Puntero a una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) que contiene información sobre el material que se va a guardar en el archivo. x.</span><span class="sxs-lookup"><span data-stu-id="70943-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="70943-123">*pEffectInstances* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-124">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="70943-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="70943-125">Puntero a una matriz de instancias de efecto, una por cada grupo de atributos de la malla.</span><span class="sxs-lookup"><span data-stu-id="70943-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="70943-126">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="70943-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="70943-127">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="70943-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="70943-128">Para obtener más información, vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="70943-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="70943-129">*NumMaterials* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70943-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70943-131">Número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *pMaterials* .</span><span class="sxs-lookup"><span data-stu-id="70943-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="70943-132">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70943-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70943-133">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70943-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70943-134">Combinación de opciones de formato de archivo y guardado al guardar un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="70943-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="70943-135">Consulte [constantes de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="70943-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70943-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70943-136">Return value</span></span>

<span data-ttu-id="70943-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70943-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70943-138">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70943-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="70943-139">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="70943-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="70943-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70943-140">Remarks</span></span>

<span data-ttu-id="70943-141">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="70943-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="70943-142">Si se define Unicode, la llamada de función se resuelve como D3DXSaveMeshToXW.</span><span class="sxs-lookup"><span data-stu-id="70943-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="70943-143">De lo contrario, la llamada de función se resuelve como D3DXSaveMeshToXA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="70943-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="70943-144">El formato de archivo predeterminado es binario; sin embargo, si se especifica un archivo como archivo binario y de texto, se guardará como un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="70943-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="70943-145">Independientemente del formato de archivo, también puede usar el formato comprimido para reducir el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="70943-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="70943-146">El siguiente es un ejemplo de código típico de cómo usar esta función.</span><span class="sxs-lookup"><span data-stu-id="70943-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="70943-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70943-147">Requirements</span></span>



| <span data-ttu-id="70943-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="70943-148">Requirement</span></span> | <span data-ttu-id="70943-149">Value</span><span class="sxs-lookup"><span data-stu-id="70943-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70943-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70943-150">Header</span></span><br/>  | <dl> <span data-ttu-id="70943-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="70943-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="70943-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70943-152">Library</span></span><br/> | <dl> <span data-ttu-id="70943-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70943-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70943-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="70943-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70943-155">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="70943-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="70943-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="70943-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="70943-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="70943-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
