---
description: La aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en los archivos. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interfaz ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717652"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="0042d-103">Interfaz ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="0042d-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="0042d-104">La aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en los archivos. x.</span><span class="sxs-lookup"><span data-stu-id="0042d-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="0042d-105">Una instancia de esta interfaz se pasa a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)y D3DX llama al método adecuado en esta interfaz cada vez que se encuentran los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="0042d-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="0042d-106">Por ejemplo, para cada objeto Frame del archivo. x, se llama a [**ID3DXLoadUserData:: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) y se pasan los datos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0042d-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="0042d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0042d-107">Members</span></span>

<span data-ttu-id="0042d-108">La interfaz **ID3DXLoadUserData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0042d-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0042d-109">**ID3DXLoadUserData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0042d-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="0042d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0042d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0042d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="0042d-111">Methods</span></span>

<span data-ttu-id="0042d-112">La interfaz **ID3DXLoadUserData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0042d-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="0042d-113">Método</span><span class="sxs-lookup"><span data-stu-id="0042d-113">Method</span></span>                                                              | <span data-ttu-id="0042d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0042d-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="0042d-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="0042d-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="0042d-116">Cargar datos secundarios de marco desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0042d-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="0042d-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="0042d-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="0042d-118">Cargar datos secundarios de la malla desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0042d-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="0042d-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="0042d-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="0042d-120">Cargue los datos de nivel superior de un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0042d-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="0042d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0042d-121">Remarks</span></span>

<span data-ttu-id="0042d-122">El tipo LPD3DXLOADUSERDATA se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0042d-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="0042d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0042d-123">Requirements</span></span>



| <span data-ttu-id="0042d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0042d-124">Requirement</span></span> | <span data-ttu-id="0042d-125">Value</span><span class="sxs-lookup"><span data-stu-id="0042d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0042d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0042d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0042d-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0042d-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0042d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0042d-128">Library</span></span><br/> | <dl> <span data-ttu-id="0042d-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0042d-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0042d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0042d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0042d-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="0042d-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
