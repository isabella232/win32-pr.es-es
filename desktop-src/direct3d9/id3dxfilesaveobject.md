---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveObject para escribir un archivo. x en el disco, y para agregar y guardar objetos y plantillas de datos.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interfaz ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717748"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="0ab2c-103">Interfaz ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="0ab2c-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="0ab2c-104">Las aplicaciones usan los métodos de la interfaz ID3DXFileSaveObject para escribir un archivo. x en el disco, y para agregar y guardar objetos y plantillas de datos.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="0ab2c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ab2c-105">Members</span></span>

<span data-ttu-id="0ab2c-106">La interfaz **ID3DXFileSaveObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0ab2c-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0ab2c-107">**ID3DXFileSaveObject** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0ab2c-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="0ab2c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ab2c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ab2c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ab2c-109">Methods</span></span>

<span data-ttu-id="0ab2c-110">La interfaz **ID3DXFileSaveObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="0ab2c-111">Método</span><span class="sxs-lookup"><span data-stu-id="0ab2c-111">Method</span></span>                                                      | <span data-ttu-id="0ab2c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ab2c-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ab2c-113">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="0ab2c-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="0ab2c-114">Agrega un objeto de datos como elemento secundario del objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="0ab2c-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="0ab2c-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="0ab2c-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="0ab2c-116">Obtiene la interfaz [**ID3DXFile**](id3dxfile.md) del objeto que creó este objeto **ID3DXFileSaveObject** .</span><span class="sxs-lookup"><span data-stu-id="0ab2c-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="0ab2c-117">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="0ab2c-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="0ab2c-118">Guarda un objeto de datos y sus elementos secundarios en un archivo. x en el disco.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0ab2c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ab2c-119">Remarks</span></span>

<span data-ttu-id="0ab2c-120">No se requieren plantillas en todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-120">Templates are not required in every file.</span></span> <span data-ttu-id="0ab2c-121">Por ejemplo, puede colocar todas las plantillas en un solo archivo. x en lugar de duplicarlas en cada archivo. x.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="0ab2c-122">La interfaz ID3DXFileSaveObject se obtiene llamando al método [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="0ab2c-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="0ab2c-123">El identificador único global (GUID) de la interfaz ID3DXFileSaveObject es IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="0ab2c-124">El tipo LPD3DXFILESAVEOBJECT se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0ab2c-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="0ab2c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ab2c-125">Requirements</span></span>



| <span data-ttu-id="0ab2c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ab2c-126">Requirement</span></span> | <span data-ttu-id="0ab2c-127">Value</span><span class="sxs-lookup"><span data-stu-id="0ab2c-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab2c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ab2c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0ab2c-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab2c-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="0ab2c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ab2c-130">Library</span></span><br/> | <dl> <span data-ttu-id="0ab2c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ab2c-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0ab2c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ab2c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab2c-133">Interfaces de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="0ab2c-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
