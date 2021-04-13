---
description: Carga una malla desde un archivo DirectX. x.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: Función D3DXLoadMeshFromX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362560"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="69655-103">D3DXLoadMeshFromX función)</span><span class="sxs-lookup"><span data-stu-id="69655-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="69655-104">Carga una malla desde un archivo DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="69655-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="69655-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69655-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="69655-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69655-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69655-107">*pFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69655-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69655-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69655-109">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="69655-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="69655-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="69655-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="69655-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="69655-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="69655-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="69655-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="69655-113">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="69655-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69655-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69655-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , que especifica las opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="69655-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="69655-116">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69655-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="69655-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="69655-118">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="69655-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="69655-119">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69655-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69655-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69655-121">Puntero a un búfer que contiene datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="69655-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="69655-122">Los datos de adyacencias contienen una matriz de tres DWORDs por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="69655-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="69655-123">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69655-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69655-124">*ppMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69655-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69655-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69655-126">Puntero a un búfer que contiene datos de materiales.</span><span class="sxs-lookup"><span data-stu-id="69655-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="69655-127">El búfer contiene una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) que contiene información del archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="69655-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="69655-128">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69655-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69655-129">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69655-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69655-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69655-131">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="69655-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="69655-132">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="69655-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="69655-133">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="69655-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="69655-134">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69655-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69655-135">*pNumMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69655-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69655-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69655-137">Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="69655-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="69655-138">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69655-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69655-139">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="69655-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="69655-140">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="69655-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69655-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69655-141">Return value</span></span>

<span data-ttu-id="69655-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69655-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69655-143">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69655-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69655-144">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="69655-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="69655-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69655-145">Remarks</span></span>

<span data-ttu-id="69655-146">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="69655-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="69655-147">Si se define Unicode, la llamada de función se resuelve como D3DXLoadMeshFromXW.</span><span class="sxs-lookup"><span data-stu-id="69655-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="69655-148">De lo contrario, la llamada de función se resuelve como D3DXLoadMeshFromXA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="69655-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="69655-149">Todas las mallas del archivo se contraen en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="69655-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="69655-150">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="69655-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="69655-151">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="69655-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="69655-152">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="69655-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="69655-153">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="69655-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="69655-154">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="69655-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="69655-155">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="69655-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="69655-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69655-156">Requirements</span></span>



| <span data-ttu-id="69655-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="69655-157">Requirement</span></span> | <span data-ttu-id="69655-158">Value</span><span class="sxs-lookup"><span data-stu-id="69655-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69655-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69655-159">Header</span></span><br/>  | <dl> <span data-ttu-id="69655-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="69655-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="69655-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69655-161">Library</span></span><br/> | <dl> <span data-ttu-id="69655-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69655-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69655-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="69655-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69655-164">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="69655-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="69655-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="69655-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="69655-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="69655-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
