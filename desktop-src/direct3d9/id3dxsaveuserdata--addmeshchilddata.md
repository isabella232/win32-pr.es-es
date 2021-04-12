---
description: Agregue datos secundarios a la malla.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'ID3DXSaveUserData:: AddMeshChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280491"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="ef489-103">ID3DXSaveUserData:: AddMeshChildData (método)</span><span class="sxs-lookup"><span data-stu-id="ef489-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="ef489-104">Agregue datos secundarios a la malla.</span><span class="sxs-lookup"><span data-stu-id="ef489-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef489-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef489-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="ef489-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef489-107">*pMeshContainer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef489-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef489-108">Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef489-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="ef489-109">Puntero a un contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="ef489-109">Pointer to a mesh container.</span></span> <span data-ttu-id="ef489-110">Vea [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ef489-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef489-111">*pXofSave* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef489-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef489-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="ef489-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="ef489-113">Puntero a un archivo. x guarda el objeto.</span><span class="sxs-lookup"><span data-stu-id="ef489-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="ef489-114">Use el puntero para llamar a [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) para agregar un objeto de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="ef489-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="ef489-115">No guarde los datos con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="ef489-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef489-116">*pXofMeshData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef489-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef489-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="ef489-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="ef489-118">Puntero a un nodo de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="ef489-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="ef489-119">Use el puntero para llamar a [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) para agregar un objeto de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="ef489-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef489-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef489-120">Return value</span></span>

<span data-ttu-id="ef489-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef489-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef489-122">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="ef489-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="ef489-123">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef489-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="ef489-124">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="ef489-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef489-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef489-125">Requirements</span></span>



| <span data-ttu-id="ef489-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef489-126">Requirement</span></span> | <span data-ttu-id="ef489-127">Value</span><span class="sxs-lookup"><span data-stu-id="ef489-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef489-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef489-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ef489-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef489-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ef489-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef489-130">Library</span></span><br/> | <dl> <span data-ttu-id="ef489-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef489-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef489-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef489-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef489-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="ef489-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
