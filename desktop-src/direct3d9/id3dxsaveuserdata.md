---
description: 'Interfaz ID3DXSaveUserData: la aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en archivos .x.'
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interfaz ID3DXSaveUserData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107183"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="ff9d5-103">Interfaz ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="ff9d5-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="ff9d5-104">Esta interfaz la implementa la aplicación para guardar los datos de usuario adicionales insertados en archivos .x.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="ff9d5-105">Una instancia de esta interfaz se pasa a [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)y D3DX llama al método adecuado en esta interfaz cada vez que se encuentran los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="ff9d5-106">Por ejemplo, para cada objeto de marco del archivo .x, se llama a [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) y se pasan los datos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="ff9d5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff9d5-107">Members</span></span>

<span data-ttu-id="ff9d5-108">La **interfaz ID3DXSaveUserData** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ff9d5-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ff9d5-109">**ID3DXSaveUserData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ff9d5-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="ff9d5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff9d5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ff9d5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff9d5-111">Methods</span></span>

<span data-ttu-id="ff9d5-112">La **interfaz ID3DXSaveUserData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="ff9d5-113">Método</span><span class="sxs-lookup"><span data-stu-id="ff9d5-113">Method</span></span>                                                                              | <span data-ttu-id="ff9d5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff9d5-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="ff9d5-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="ff9d5-116">Agregue datos secundarios al marco.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="ff9d5-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="ff9d5-118">Agregue datos secundarios a la malla.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="ff9d5-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="ff9d5-120">Agregue un objeto de nivel superior después de la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="ff9d5-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="ff9d5-122">Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="ff9d5-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="ff9d5-124">Devolución de llamada para que el usuario registre una plantilla de archivo .x.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="ff9d5-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="ff9d5-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="ff9d5-126">Devolución de llamada para que el usuario guarde una plantilla de archivo .x.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ff9d5-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff9d5-127">Remarks</span></span>

<span data-ttu-id="ff9d5-128">El tipo LPD3DXSAVEUSERDATA se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="ff9d5-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="ff9d5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff9d5-129">Requirements</span></span>



| <span data-ttu-id="ff9d5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff9d5-130">Requirement</span></span> | <span data-ttu-id="ff9d5-131">Value</span><span class="sxs-lookup"><span data-stu-id="ff9d5-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9d5-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff9d5-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ff9d5-133"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="ff9d5-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ff9d5-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff9d5-134">Library</span></span><br/> | <dl> <span data-ttu-id="ff9d5-135"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff9d5-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff9d5-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff9d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9d5-137">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="ff9d5-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
