---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer en iteración los objetos de datos de archivo secundarios en el archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaz ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003871"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="f94d7-103">Interfaz ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="f94d7-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="f94d7-104">Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer en iteración los objetos de datos de archivo secundarios en el archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.</span><span class="sxs-lookup"><span data-stu-id="f94d7-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="f94d7-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f94d7-105">Members</span></span>

<span data-ttu-id="f94d7-106">La interfaz **ID3DXFileEnumObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f94d7-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f94d7-107">**ID3DXFileEnumObject** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f94d7-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="f94d7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f94d7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f94d7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f94d7-109">Methods</span></span>

<span data-ttu-id="f94d7-110">La interfaz **ID3DXFileEnumObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f94d7-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="f94d7-111">Método</span><span class="sxs-lookup"><span data-stu-id="f94d7-111">Method</span></span>                                                                  | <span data-ttu-id="f94d7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f94d7-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="f94d7-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="f94d7-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="f94d7-114">Recupera un objeto secundario en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f94d7-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="f94d7-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="f94d7-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="f94d7-116">Recupera el número de objetos secundarios de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f94d7-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="f94d7-117">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="f94d7-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="f94d7-118">Recupera el objeto de datos que tiene el GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="f94d7-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="f94d7-119">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="f94d7-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="f94d7-120">Recupera el objeto de datos que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="f94d7-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="f94d7-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="f94d7-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="f94d7-122">Recupera el objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f94d7-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="f94d7-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f94d7-123">Remarks</span></span>

<span data-ttu-id="f94d7-124">El GUID de la interfaz ID3DXFileEnumObject es IID \_ ID3DXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="f94d7-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="f94d7-125">El tipo LPD3DXFILEENUMOBJECT se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="f94d7-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="f94d7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f94d7-126">Requirements</span></span>



| <span data-ttu-id="f94d7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f94d7-127">Requirement</span></span> | <span data-ttu-id="f94d7-128">Value</span><span class="sxs-lookup"><span data-stu-id="f94d7-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f94d7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f94d7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f94d7-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94d7-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f94d7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f94d7-131">Library</span></span><br/> | <dl> <span data-ttu-id="f94d7-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f94d7-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f94d7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f94d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94d7-134">Interfaces de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="f94d7-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
