---
description: Una devolución de llamada para que el usuario guarde una plantilla de archivo. x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'ID3DXSaveUserData:: SaveTemplates (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003964"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="77af5-103">ID3DXSaveUserData:: SaveTemplates (método)</span><span class="sxs-lookup"><span data-stu-id="77af5-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="77af5-104">Una devolución de llamada para que el usuario guarde una plantilla de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="77af5-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="77af5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77af5-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="77af5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77af5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77af5-107">*pXofSave* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77af5-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77af5-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="77af5-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="77af5-109">Puntero a un archivo. x guarda el objeto.</span><span class="sxs-lookup"><span data-stu-id="77af5-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="77af5-110">No use este parámetro para agregar objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="77af5-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="77af5-111">Vea [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="77af5-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77af5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77af5-112">Return value</span></span>

<span data-ttu-id="77af5-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77af5-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77af5-114">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="77af5-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="77af5-115">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77af5-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="77af5-116">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="77af5-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="77af5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77af5-117">Remarks</span></span>

<span data-ttu-id="77af5-118">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) y **ID3DXSaveUserData:: SaveTemplates** proporcionan un mecanismo para agregar una plantilla a un archivo. x para guardar los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="77af5-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="77af5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77af5-119">Requirements</span></span>



| <span data-ttu-id="77af5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77af5-120">Requirement</span></span> | <span data-ttu-id="77af5-121">Value</span><span class="sxs-lookup"><span data-stu-id="77af5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77af5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77af5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="77af5-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="77af5-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="77af5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77af5-124">Library</span></span><br/> | <dl> <span data-ttu-id="77af5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77af5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77af5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="77af5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77af5-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="77af5-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
