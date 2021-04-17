---
description: Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'ID3DXSaveUserData:: AddTopLevelDataObjectsPre (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670259"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="fa826-103">ID3DXSaveUserData:: AddTopLevelDataObjectsPre (método)</span><span class="sxs-lookup"><span data-stu-id="fa826-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="fa826-104">Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="fa826-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa826-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa826-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="fa826-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa826-107">*pXofSave* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fa826-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa826-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="fa826-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="fa826-109">Puntero a un archivo. x guarda el objeto.</span><span class="sxs-lookup"><span data-stu-id="fa826-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="fa826-110">Use este puntero para llamar a [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear el objeto de datos que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="fa826-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="fa826-111">A continuación, llame a [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md) para guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="fa826-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa826-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa826-112">Return value</span></span>

<span data-ttu-id="fa826-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa826-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa826-114">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="fa826-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="fa826-115">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa826-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="fa826-116">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="fa826-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa826-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa826-117">Requirements</span></span>



| <span data-ttu-id="fa826-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa826-118">Requirement</span></span> | <span data-ttu-id="fa826-119">Value</span><span class="sxs-lookup"><span data-stu-id="fa826-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa826-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa826-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fa826-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa826-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fa826-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa826-122">Library</span></span><br/> | <dl> <span data-ttu-id="fa826-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa826-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa826-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa826-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa826-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="fa826-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
