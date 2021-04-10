---
description: Agregue datos secundarios al marco.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData:: AddFrameChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280492"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="0bc5d-103">ID3DXSaveUserData:: AddFrameChildData (método)</span><span class="sxs-lookup"><span data-stu-id="0bc5d-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="0bc5d-104">Agregue datos secundarios al marco.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bc5d-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="0bc5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bc5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc5d-107">*pFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bc5d-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc5d-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bc5d-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="0bc5d-109">Puntero a un contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-109">Pointer to a mesh container.</span></span> <span data-ttu-id="0bc5d-110">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="0bc5d-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc5d-111">*pXofSave* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bc5d-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc5d-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc5d-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="0bc5d-113">Puntero a un archivo. x guarda el objeto.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="0bc5d-114">Use el puntero para llamar a [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) para agregar un objeto de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="0bc5d-115">No guarde los datos con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="0bc5d-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc5d-116">*pXofFrameData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bc5d-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc5d-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc5d-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="0bc5d-118">Puntero a un nodo de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="0bc5d-119">Use el puntero para llamar a [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) para agregar un objeto de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc5d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bc5d-120">Return value</span></span>

<span data-ttu-id="0bc5d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bc5d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bc5d-122">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0bc5d-123">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0bc5d-124">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc5d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bc5d-125">Remarks</span></span>

<span data-ttu-id="0bc5d-126">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) y [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) proporcionan un mecanismo para agregar una plantilla a un archivo. x para guardar los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="0bc5d-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc5d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bc5d-127">Requirements</span></span>



| <span data-ttu-id="0bc5d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bc5d-128">Requirement</span></span> | <span data-ttu-id="0bc5d-129">Value</span><span class="sxs-lookup"><span data-stu-id="0bc5d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc5d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bc5d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc5d-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc5d-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc5d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bc5d-132">Library</span></span><br/> | <dl> <span data-ttu-id="0bc5d-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc5d-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bc5d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bc5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc5d-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="0bc5d-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
