---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveData para agregar objetos de datos como elementos secundarios de un nodo de datos de archivo. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interfaz ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698236"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="2a152-103">Interfaz ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="2a152-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="2a152-104">Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveData para agregar objetos de datos como elementos secundarios de un nodo de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="2a152-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="2a152-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a152-105">Members</span></span>

<span data-ttu-id="2a152-106">La interfaz **ID3DXFileSaveData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2a152-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2a152-107">**ID3DXFileSaveData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2a152-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="2a152-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2a152-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2a152-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2a152-109">Methods</span></span>

<span data-ttu-id="2a152-110">La interfaz **ID3DXFileSaveData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2a152-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="2a152-111">Método</span><span class="sxs-lookup"><span data-stu-id="2a152-111">Method</span></span>                                                          | <span data-ttu-id="2a152-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a152-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a152-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="2a152-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="2a152-114">Agrega un objeto de datos como elemento secundario del nodo de datos del archivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="2a152-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="2a152-115">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="2a152-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="2a152-116">Agrega una referencia de datos como un elemento secundario de este nodo de datos de archivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="2a152-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="2a152-117">La referencia de datos apunta a un objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2a152-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="2a152-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="2a152-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="2a152-119">Recupera el GUID de este nodo de datos del archivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="2a152-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="2a152-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="2a152-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="2a152-121">Recupera el nombre de este nodo de datos del archivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="2a152-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="2a152-122">**GetSave**</span><span class="sxs-lookup"><span data-stu-id="2a152-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="2a152-123">Recupera un puntero a este nodo de datos del archivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="2a152-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="2a152-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="2a152-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="2a152-125">Recupera el identificador de plantilla de este nodo de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2a152-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="2a152-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a152-126">Remarks</span></span>

<span data-ttu-id="2a152-127">El GUID de la interfaz ID3DXFileSaveObject es IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="2a152-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="2a152-128">El tipo LPD3DXFileSaveData se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2a152-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="2a152-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a152-129">Requirements</span></span>



| <span data-ttu-id="2a152-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a152-130">Requirement</span></span> | <span data-ttu-id="2a152-131">Value</span><span class="sxs-lookup"><span data-stu-id="2a152-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a152-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a152-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2a152-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a152-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2a152-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a152-134">Library</span></span><br/> | <dl> <span data-ttu-id="2a152-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a152-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2a152-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a152-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a152-137">Interfaces de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="2a152-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
