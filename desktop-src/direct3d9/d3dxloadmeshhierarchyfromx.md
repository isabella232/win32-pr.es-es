---
description: Carga la primera jerarquía de fotogramas desde un archivo. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Función D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003767"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="19191-103">D3DXLoadMeshHierarchyFromX función)</span><span class="sxs-lookup"><span data-stu-id="19191-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="19191-104">Carga la primera jerarquía de fotogramas desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="19191-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="19191-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19191-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="19191-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19191-107">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19191-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19191-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19191-109">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="19191-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="19191-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="19191-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="19191-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="19191-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="19191-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="19191-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19191-113">*MeshOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19191-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19191-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19191-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="19191-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="19191-116">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19191-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="19191-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="19191-118">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="19191-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="19191-119">*pAlloc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19191-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="19191-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="19191-121">Puntero a una interfaz [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="19191-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="19191-122">*pUserDataLoader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19191-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="19191-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="19191-124">Interfaz proporcionada por la aplicación que permite cargar datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="19191-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="19191-125">Vea [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="19191-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="19191-126">*ppFrameHierarchy* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19191-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="19191-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="19191-128">Devuelve un puntero a la jerarquía de Marcos cargada.</span><span class="sxs-lookup"><span data-stu-id="19191-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="19191-129">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="19191-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="19191-130">*ppAnimController* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19191-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19191-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="19191-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="19191-132">Devuelve un puntero al controlador de animación correspondiente a la animación en el archivo. x.</span><span class="sxs-lookup"><span data-stu-id="19191-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="19191-133">Se crea con pistas y eventos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="19191-133">This is created with default tracks and events.</span></span> <span data-ttu-id="19191-134">Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="19191-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19191-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19191-135">Return value</span></span>

<span data-ttu-id="19191-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19191-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19191-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19191-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19191-138">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19191-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19191-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19191-139">Remarks</span></span>

<span data-ttu-id="19191-140">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="19191-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="19191-141">Si se define Unicode, la llamada de función se resuelve como D3DXLoadMeshHierarchyFromXW.</span><span class="sxs-lookup"><span data-stu-id="19191-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="19191-142">De lo contrario, la llamada de función se resuelve como D3DXLoadMeshHierarchyFromXA.</span><span class="sxs-lookup"><span data-stu-id="19191-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="19191-143">Todas las mallas del archivo se contraen en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="19191-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="19191-144">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="19191-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="19191-145">**D3DXLoadMeshHierarchyFromX** carga los datos de animación y la jerarquía de Marcos desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="19191-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="19191-146">Examina el archivo. x y crea una jerarquía de Marcos y un controlador de animación según el objeto derivado de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)que se le pasa a través de pAlloc.</span><span class="sxs-lookup"><span data-stu-id="19191-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="19191-147">La carga de los datos requiere varios pasos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="19191-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="19191-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando cada método.</span><span class="sxs-lookup"><span data-stu-id="19191-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="19191-149">Controla cómo se asignan y liberan los fotogramas y las mallas.</span><span class="sxs-lookup"><span data-stu-id="19191-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="19191-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando cada método.</span><span class="sxs-lookup"><span data-stu-id="19191-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="19191-151">Si el archivo. x no tiene datos incrustados definidos por el usuario, o si no lo necesita, puede omitir esta parte.</span><span class="sxs-lookup"><span data-stu-id="19191-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="19191-152">Cree un objeto de la clase [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y, opcionalmente, de la clase LoadUserData.</span><span class="sxs-lookup"><span data-stu-id="19191-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="19191-153">No es necesario llamar a los métodos de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="19191-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="19191-154">Llame a **D3DXLoadMeshHierarchyFromX**, pasando el objeto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) y el objeto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (o **null**) para crear la jerarquía de fotogramas y el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="19191-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="19191-155">Todos los marcos y conjuntos de animaciones se registran automáticamente en el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="19191-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="19191-156">Durante la carga, se vuelve a llamar a [**CreateFrame**](id3dxallocatehierarchy--createframe.md) y [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) en cada fotograma para controlar la carga y la asignación del marco.</span><span class="sxs-lookup"><span data-stu-id="19191-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="19191-157">La aplicación define estos métodos para controlar cómo se almacenan los marcos.</span><span class="sxs-lookup"><span data-stu-id="19191-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="19191-158">Se vuelve a llamar a [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) y [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) en cada objeto Mesh para controlar la carga y la asignación de objetos Mesh.</span><span class="sxs-lookup"><span data-stu-id="19191-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="19191-159">Se vuelve a llamar a [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) para cada objeto de nivel superior que no se carga mediante otros métodos.</span><span class="sxs-lookup"><span data-stu-id="19191-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="19191-160">Para liberar estos datos, llame a ID3DXAnimationController:: release para liberar los conjuntos de animaciones y [**D3DXFRAMEDestroy**](d3dxframedestroy.md), pasando el nodo raíz de la jerarquía de Marcos y un objeto de la clase [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivada.</span><span class="sxs-lookup"><span data-stu-id="19191-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="19191-161">Se llamará a [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) y [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) para cada fotograma y objeto de malla en la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="19191-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="19191-162">La implementación de **DestroyFrame** debe liberar todo lo asignado por [**CreateFrame**](id3dxallocatehierarchy--createframe.md)y, igualmente, para los métodos de contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="19191-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="19191-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19191-163">Requirements</span></span>



| <span data-ttu-id="19191-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="19191-164">Requirement</span></span> | <span data-ttu-id="19191-165">Value</span><span class="sxs-lookup"><span data-stu-id="19191-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19191-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19191-166">Header</span></span><br/>  | <dl> <span data-ttu-id="19191-167"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="19191-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="19191-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19191-168">Library</span></span><br/> | <dl> <span data-ttu-id="19191-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19191-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19191-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="19191-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19191-171">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="19191-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
