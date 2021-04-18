---
description: Cargue los datos de nivel superior de un archivo. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData:: LoadTopLevelData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718457"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="7080e-103">ID3DXLoadUserData:: LoadTopLevelData (método)</span><span class="sxs-lookup"><span data-stu-id="7080e-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="7080e-104">Cargue los datos de nivel superior de un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="7080e-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7080e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7080e-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="7080e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7080e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7080e-107">*pXofChildData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7080e-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7080e-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="7080e-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="7080e-109">Puntero a una estructura de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="7080e-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="7080e-110">Esto se define en Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="7080e-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7080e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7080e-111">Return value</span></span>

<span data-ttu-id="7080e-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7080e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7080e-113">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="7080e-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7080e-114">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7080e-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7080e-115">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="7080e-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7080e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7080e-116">Requirements</span></span>



| <span data-ttu-id="7080e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7080e-117">Requirement</span></span> | <span data-ttu-id="7080e-118">Value</span><span class="sxs-lookup"><span data-stu-id="7080e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7080e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7080e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7080e-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7080e-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7080e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7080e-121">Library</span></span><br/> | <dl> <span data-ttu-id="7080e-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7080e-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7080e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7080e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7080e-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="7080e-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




