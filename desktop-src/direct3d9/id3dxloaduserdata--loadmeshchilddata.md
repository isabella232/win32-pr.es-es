---
description: Cargar datos secundarios de la malla desde un archivo. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'ID3DXLoadUserData:: LoadMeshChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717656"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="47c8f-103">ID3DXLoadUserData:: LoadMeshChildData (método)</span><span class="sxs-lookup"><span data-stu-id="47c8f-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="47c8f-104">Cargar datos secundarios de la malla desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="47c8f-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47c8f-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="47c8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47c8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c8f-107">*pMeshContainer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47c8f-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c8f-108">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="47c8f-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="47c8f-109">Puntero a un contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="47c8f-109">Pointer to a mesh container.</span></span> <span data-ttu-id="47c8f-110">Vea [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="47c8f-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c8f-111">*pXofChildData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47c8f-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c8f-112">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="47c8f-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="47c8f-113">Puntero a una estructura de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="47c8f-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="47c8f-114">Esto se define en Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="47c8f-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c8f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47c8f-115">Return value</span></span>

<span data-ttu-id="47c8f-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47c8f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47c8f-117">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="47c8f-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="47c8f-118">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47c8f-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="47c8f-119">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="47c8f-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c8f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c8f-120">Requirements</span></span>



| <span data-ttu-id="47c8f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c8f-121">Requirement</span></span> | <span data-ttu-id="47c8f-122">Value</span><span class="sxs-lookup"><span data-stu-id="47c8f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c8f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47c8f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="47c8f-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c8f-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="47c8f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47c8f-125">Library</span></span><br/> | <dl> <span data-ttu-id="47c8f-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47c8f-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47c8f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="47c8f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c8f-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="47c8f-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




