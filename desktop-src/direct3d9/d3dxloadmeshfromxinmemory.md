---
description: Carga una malla de la memoria.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Función D3DXLoadMeshFromXInMemory (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707875"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="1b8f1-103">D3DXLoadMeshFromXInMemory función)</span><span class="sxs-lookup"><span data-stu-id="1b8f1-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="1b8f1-104">Carga una malla de la memoria.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b8f1-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1b8f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b8f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8f1-107">*Memoria* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b8f1-109">Puntero al búfer de memoria que contiene los datos de la malla.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-110">*SizeOfMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b8f1-112">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-113">*Opciones* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b8f1-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-116">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1b8f1-118">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-119">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8f1-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1b8f1-121">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8f1-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1b8f1-122">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-123">*ppMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8f1-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1b8f1-125">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8f1-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1b8f1-126">Cuando este método finaliza, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) , que contiene información guardada en el archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-127">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8f1-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1b8f1-129">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="1b8f1-130">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="1b8f1-131">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="1b8f1-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="1b8f1-132">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1b8f1-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-133">*pNumMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8f1-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1b8f1-135">Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="1b8f1-136">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b8f1-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8f1-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8f1-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1b8f1-138">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8f1-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b8f1-139">Return value</span></span>

<span data-ttu-id="1b8f1-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b8f1-141">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1b8f1-142">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8f1-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b8f1-143">Remarks</span></span>

<span data-ttu-id="1b8f1-144">Todas las mallas del archivo se contraen en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="1b8f1-145">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="1b8f1-146">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="1b8f1-147">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8f1-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="1b8f1-148">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="1b8f1-149">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="1b8f1-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="1b8f1-150">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="1b8f1-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8f1-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b8f1-151">Requirements</span></span>



| <span data-ttu-id="1b8f1-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b8f1-152">Requirement</span></span> | <span data-ttu-id="1b8f1-153">Value</span><span class="sxs-lookup"><span data-stu-id="1b8f1-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8f1-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b8f1-154">Header</span></span><br/>  | <dl> <span data-ttu-id="1b8f1-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8f1-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1b8f1-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b8f1-156">Library</span></span><br/> | <dl> <span data-ttu-id="1b8f1-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b8f1-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b8f1-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b8f1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8f1-159">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="1b8f1-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1b8f1-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="1b8f1-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="1b8f1-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
