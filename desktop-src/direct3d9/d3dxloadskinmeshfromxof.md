---
description: Carga una malla de máscara desde un objeto de datos de archivo de DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Función D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820954"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="759bc-103">D3DXLoadSkinMeshFromXof función)</span><span class="sxs-lookup"><span data-stu-id="759bc-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="759bc-104">Carga una malla de máscara desde un objeto de datos de archivo de DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="759bc-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="759bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="759bc-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="759bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="759bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="759bc-107">*pxofMesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="759bc-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="759bc-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="759bc-109">Puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="759bc-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-110">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="759bc-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="759bc-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="759bc-112">Combinación de una o varias marcas, de la enumeración [**D3DXMESH**](./d3dxmesh.md) , que especifica las opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="759bc-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-113">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="759bc-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="759bc-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="759bc-115">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="759bc-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-116">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="759bc-118">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="759bc-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="759bc-119">Cuando este método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="759bc-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-120">*ppMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="759bc-122">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="759bc-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="759bc-123">Cuando el método finaliza, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="759bc-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-124">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="759bc-126">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="759bc-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="759bc-127">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="759bc-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="759bc-128">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="759bc-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="759bc-129">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="759bc-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="759bc-130">*pMatOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="759bc-132">Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="759bc-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-133">*ppSkinInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-134">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="759bc-135">Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa la información de la piel.</span><span class="sxs-lookup"><span data-stu-id="759bc-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="759bc-136">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="759bc-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="759bc-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="759bc-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="759bc-138">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) , que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="759bc-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="759bc-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="759bc-139">Return value</span></span>

<span data-ttu-id="759bc-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="759bc-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="759bc-141">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="759bc-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="759bc-142">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="759bc-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="759bc-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="759bc-143">Remarks</span></span>

<span data-ttu-id="759bc-144">Este método toma un puntero a un objeto interno en el archivo. x, lo que le permite cargar la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="759bc-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="759bc-145">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="759bc-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="759bc-146">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="759bc-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="759bc-147">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="759bc-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="759bc-148">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="759bc-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="759bc-149">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="759bc-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="759bc-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="759bc-150">Requirements</span></span>



| <span data-ttu-id="759bc-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="759bc-151">Requirement</span></span> | <span data-ttu-id="759bc-152">Value</span><span class="sxs-lookup"><span data-stu-id="759bc-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="759bc-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="759bc-153">Header</span></span><br/>  | <dl> <span data-ttu-id="759bc-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="759bc-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="759bc-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="759bc-155">Library</span></span><br/> | <dl> <span data-ttu-id="759bc-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="759bc-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="759bc-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="759bc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759bc-158">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="759bc-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="759bc-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="759bc-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="759bc-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="759bc-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
