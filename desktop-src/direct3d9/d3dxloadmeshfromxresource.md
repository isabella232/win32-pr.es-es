---
description: Carga una malla desde un recurso.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Función D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821063"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="0e4d9-103">D3DXLoadMeshFromXResource función)</span><span class="sxs-lookup"><span data-stu-id="0e4d9-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="0e4d9-104">Carga una malla desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e4d9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="0e4d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e4d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e4d9-107">*Módulo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e4d9-109">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="0e4d9-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-111">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e4d9-113">Puntero a una cadena que especifica el recurso del que se va a crear la malla.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="0e4d9-114">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-115">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e4d9-117">Puntero a una cadena que especifica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="0e4d9-118">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-119">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e4d9-121">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-122">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0e4d9-124">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-125">*ppAdjacency* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e4d9-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0e4d9-127">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0e4d9-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0e4d9-128">Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-129">*ppMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e4d9-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0e4d9-131">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0e4d9-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0e4d9-132">Cuando este método finaliza, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) , que contiene información guardada en el archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-133">*ppEffectInstances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e4d9-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0e4d9-135">Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="0e4d9-136">Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="0e4d9-137">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="0e4d9-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="0e4d9-138">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0e4d9-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-139">*pNumMaterials* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e4d9-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0e4d9-141">Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="0e4d9-142">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e4d9-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d9-143">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e4d9-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0e4d9-144">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla cargada.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e4d9-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e4d9-145">Return value</span></span>

<span data-ttu-id="0e4d9-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e4d9-147">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e4d9-148">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e4d9-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e4d9-149">Remarks</span></span>

<span data-ttu-id="0e4d9-150">Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para obtener más información sobre el módulo, el nombre y los parámetros de tipo.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="0e4d9-151">Todas las mallas del archivo se contraen en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="0e4d9-152">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="0e4d9-153">En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="0e4d9-154">Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="0e4d9-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="0e4d9-155">El nombre de textura predeterminado también se rellena, pero se trata de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="0e4d9-156">El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre".</span><span class="sxs-lookup"><span data-stu-id="0e4d9-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="0e4d9-157">Esto contendrá el nombre del archivo de cadena para la textura.</span><span class="sxs-lookup"><span data-stu-id="0e4d9-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e4d9-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e4d9-158">Requirements</span></span>



| <span data-ttu-id="0e4d9-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e4d9-159">Requirement</span></span> | <span data-ttu-id="0e4d9-160">Value</span><span class="sxs-lookup"><span data-stu-id="0e4d9-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4d9-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e4d9-161">Header</span></span><br/>  | <dl> <span data-ttu-id="0e4d9-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d9-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0e4d9-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e4d9-163">Library</span></span><br/> | <dl> <span data-ttu-id="0e4d9-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d9-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e4d9-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e4d9-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e4d9-166">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="0e4d9-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="0e4d9-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="0e4d9-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0e4d9-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
