---
description: Carga una malla desde un objeto ID3DXFileData.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: Función D3DXLoadMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362559"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="f191e-103">D3DXLoadMeshFromXof función)</span><span class="sxs-lookup"><span data-stu-id="f191e-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="f191e-104">Carga una malla desde un objeto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="f191e-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f191e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f191e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f191e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f191e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f191e-107">*pxofMesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f191e-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="f191e-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="f191e-109">Puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="f191e-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="f191e-110">*Opciones* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f191e-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f191e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f191e-112">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="f191e-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f191e-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f191e-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f191e-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f191e-115">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="f191e-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f191e-116">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f191e-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f191e-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f191e-118">Puntero a un búfer que contiene datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="f191e-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="f191e-119">Los datos de adyacencias contienen una matriz de tres DWORDs por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="f191e-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="f191e-120">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f191e-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="f191e-121">*ppMaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f191e-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f191e-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f191e-123">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f191e-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="f191e-124">Cuando el método finaliza, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="f191e-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="f191e-125">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f191e-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f191e-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f191e-127">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="f191e-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="f191e-128">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="f191e-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="f191e-129">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="f191e-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="f191e-130">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f191e-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="f191e-131">*pNumMaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f191e-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f191e-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f191e-133">Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="f191e-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="f191e-134">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f191e-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f191e-135">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f191e-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="f191e-136">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="f191e-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f191e-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f191e-137">Return value</span></span>

<span data-ttu-id="f191e-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f191e-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f191e-139">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f191e-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f191e-140">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f191e-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f191e-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f191e-141">Remarks</span></span>

<span data-ttu-id="f191e-142">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="f191e-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="f191e-143">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="f191e-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="f191e-144">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="f191e-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="f191e-145">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="f191e-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="f191e-146">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="f191e-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="f191e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f191e-147">Requirements</span></span>



| <span data-ttu-id="f191e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f191e-148">Requirement</span></span> | <span data-ttu-id="f191e-149">Value</span><span class="sxs-lookup"><span data-stu-id="f191e-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f191e-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f191e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="f191e-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f191e-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f191e-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f191e-152">Library</span></span><br/> | <dl> <span data-ttu-id="f191e-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f191e-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f191e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f191e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f191e-155">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="f191e-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f191e-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f191e-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="f191e-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="f191e-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
