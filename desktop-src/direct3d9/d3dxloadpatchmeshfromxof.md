---
description: Carga una malla de revisión desde un objeto ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Función D3DXLoadPatchMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707839"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="d2206-103">D3DXLoadPatchMeshFromXof función)</span><span class="sxs-lookup"><span data-stu-id="d2206-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="d2206-104">Carga una malla de revisión desde un objeto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="d2206-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2206-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2206-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d2206-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2206-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2206-107">*pxofMesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2206-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="d2206-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="d2206-109">Puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="d2206-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="d2206-110">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d2206-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2206-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2206-112">Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="d2206-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d2206-113">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2206-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d2206-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d2206-115">Puntero al dispositivo desde el que se crea la malla.</span><span class="sxs-lookup"><span data-stu-id="d2206-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="d2206-116">*ppMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d2206-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2206-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d2206-118">Matriz de materiales incluidos en la malla.</span><span class="sxs-lookup"><span data-stu-id="d2206-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="d2206-119">Cada material se indexa mediante una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d2206-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d2206-120">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d2206-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2206-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d2206-122">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="d2206-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="d2206-123">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="d2206-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="d2206-124">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="d2206-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="d2206-125">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="d2206-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2206-126">*pNumMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d2206-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-127">Tipo: **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="d2206-127">Type: **PDWORD**</span></span>

<span data-ttu-id="d2206-128">Puntero que contiene el número de materiales en la malla.</span><span class="sxs-lookup"><span data-stu-id="d2206-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d2206-129">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d2206-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2206-130">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2206-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="d2206-131">Dirección de un puntero a una interfaz [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="d2206-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2206-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2206-132">Return value</span></span>

<span data-ttu-id="d2206-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2206-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2206-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2206-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2206-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d2206-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2206-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2206-136">Remarks</span></span>

<span data-ttu-id="d2206-137">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="d2206-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="d2206-138">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="d2206-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="d2206-139">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="d2206-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="d2206-140">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="d2206-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="d2206-141">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="d2206-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2206-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2206-142">Requirements</span></span>



| <span data-ttu-id="d2206-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2206-143">Requirement</span></span> | <span data-ttu-id="d2206-144">Value</span><span class="sxs-lookup"><span data-stu-id="d2206-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2206-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2206-145">Header</span></span><br/>  | <dl> <span data-ttu-id="d2206-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2206-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2206-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2206-147">Library</span></span><br/> | <dl> <span data-ttu-id="d2206-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2206-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2206-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2206-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2206-150">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="d2206-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d2206-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d2206-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="d2206-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="d2206-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
