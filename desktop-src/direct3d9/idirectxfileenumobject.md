---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileEnumObject para recorrer en iteración los objetos de datos en el archivo y para recuperar un objeto de datos por su identificador único global (GUID) o por su nombre. En desuso.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interfaz IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689877"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="59eba-104">Interfaz IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="59eba-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="59eba-105">Las aplicaciones usan los métodos de la interfaz IDirectXFileEnumObject para recorrer en iteración los objetos de datos en el archivo y para recuperar un objeto de datos por su identificador único global (GUID) o por su nombre.</span><span class="sxs-lookup"><span data-stu-id="59eba-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="59eba-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="59eba-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="59eba-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="59eba-107">Members</span></span>

<span data-ttu-id="59eba-108">La interfaz **IDirectXFileEnumObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="59eba-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="59eba-109">**IDirectXFileEnumObject** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="59eba-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="59eba-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="59eba-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59eba-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="59eba-111">Methods</span></span>

<span data-ttu-id="59eba-112">La interfaz **IDirectXFileEnumObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="59eba-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="59eba-113">Método</span><span class="sxs-lookup"><span data-stu-id="59eba-113">Method</span></span>                                                                     | <span data-ttu-id="59eba-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="59eba-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="59eba-115">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="59eba-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="59eba-116">Recupera el objeto de datos que tiene el GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="59eba-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="59eba-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="59eba-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="59eba-118">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="59eba-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="59eba-119">Recupera el objeto de datos que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="59eba-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="59eba-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="59eba-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="59eba-121">**GetNextDataObject**</span><span class="sxs-lookup"><span data-stu-id="59eba-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="59eba-122">Recupera el siguiente objeto de nivel superior en el archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="59eba-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="59eba-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="59eba-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59eba-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59eba-124">Remarks</span></span>

<span data-ttu-id="59eba-125">El GUID de la interfaz IDirectXFileEnumObject es IID \_ IDirectXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="59eba-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="59eba-126">El tipo LPDIRECTXFILEENUMOBJECT se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="59eba-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="59eba-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59eba-127">Requirements</span></span>



| <span data-ttu-id="59eba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="59eba-128">Requirement</span></span> | <span data-ttu-id="59eba-129">Value</span><span class="sxs-lookup"><span data-stu-id="59eba-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59eba-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59eba-130">Header</span></span><br/>  | <dl> <span data-ttu-id="59eba-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="59eba-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="59eba-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59eba-132">Library</span></span><br/> | <dl> <span data-ttu-id="59eba-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59eba-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eba-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="59eba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eba-135">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="59eba-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
