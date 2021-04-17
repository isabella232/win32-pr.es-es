---
description: Una devolución de llamada para que el usuario registre una plantilla de archivo. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData:: RegisterTemplates (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718479"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="f7eff-103">ID3DXSaveUserData:: RegisterTemplates (método)</span><span class="sxs-lookup"><span data-stu-id="f7eff-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="f7eff-104">Una devolución de llamada para que el usuario registre una plantilla de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="f7eff-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7eff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7eff-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="f7eff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7eff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7eff-107">*pXFileApi* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7eff-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7eff-108">Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eff-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="f7eff-109">Use este puntero para registrar plantillas de archivo. x definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f7eff-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="f7eff-110">Vea [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="f7eff-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="f7eff-111">No use este parámetro para agregar objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="f7eff-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7eff-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7eff-112">Return value</span></span>

<span data-ttu-id="f7eff-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7eff-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7eff-114">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="f7eff-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f7eff-115">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7eff-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f7eff-116">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="f7eff-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7eff-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7eff-117">Remarks</span></span>

<span data-ttu-id="f7eff-118">**ID3DXSaveUserData:: RegisterTemplates** y [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) proporcionan un mecanismo para agregar una plantilla a un archivo. x para guardar los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="f7eff-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7eff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7eff-119">Requirements</span></span>



| <span data-ttu-id="f7eff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7eff-120">Requirement</span></span> | <span data-ttu-id="f7eff-121">Value</span><span class="sxs-lookup"><span data-stu-id="f7eff-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eff-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7eff-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f7eff-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7eff-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f7eff-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7eff-124">Library</span></span><br/> | <dl> <span data-ttu-id="f7eff-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7eff-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7eff-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7eff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7eff-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="f7eff-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
