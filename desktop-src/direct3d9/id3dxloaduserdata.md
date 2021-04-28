---
description: 'Interfaz ID3DXLoadUserData: la aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en archivos .x.'
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interfaz ID3DXLoadUserData (D3dx9anim.h)
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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093633"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="d1893-103">Interfaz ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="d1893-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="d1893-104">Esta interfaz la implementa la aplicación para guardar los datos de usuario adicionales insertados en archivos .x.</span><span class="sxs-lookup"><span data-stu-id="d1893-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="d1893-105">Una instancia de esta interfaz se pasa a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)y D3DX llama al método adecuado en esta interfaz cada vez que se encuentran los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="d1893-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="d1893-106">Por ejemplo, para cada objeto de marco del archivo .x, se llama a [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) y se pasan los datos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d1893-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="d1893-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1893-107">Members</span></span>

<span data-ttu-id="d1893-108">La **interfaz ID3DXLoadUserData** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="d1893-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d1893-109">**ID3DXLoadUserData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1893-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="d1893-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1893-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1893-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1893-111">Methods</span></span>

<span data-ttu-id="d1893-112">La **interfaz ID3DXLoadUserData tiene** estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d1893-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="d1893-113">Método</span><span class="sxs-lookup"><span data-stu-id="d1893-113">Method</span></span>                                                              | <span data-ttu-id="d1893-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1893-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="d1893-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="d1893-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="d1893-116">Cargar datos secundarios de marco desde un archivo .x.</span><span class="sxs-lookup"><span data-stu-id="d1893-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="d1893-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="d1893-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="d1893-118">Carga de datos secundarios de malla desde un archivo .x.</span><span class="sxs-lookup"><span data-stu-id="d1893-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="d1893-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="d1893-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="d1893-120">Cargar datos de nivel superior desde un archivo .x.</span><span class="sxs-lookup"><span data-stu-id="d1893-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="d1893-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1893-121">Remarks</span></span>

<span data-ttu-id="d1893-122">El tipo LPD3DXLOADUSERDATA se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d1893-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="d1893-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1893-123">Requirements</span></span>



| <span data-ttu-id="d1893-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1893-124">Requirement</span></span> | <span data-ttu-id="d1893-125">Value</span><span class="sxs-lookup"><span data-stu-id="d1893-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1893-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1893-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d1893-127"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="d1893-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d1893-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1893-128">Library</span></span><br/> | <dl> <span data-ttu-id="d1893-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1893-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1893-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d1893-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1893-131">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="d1893-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
