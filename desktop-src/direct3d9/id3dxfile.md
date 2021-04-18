---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFile para crear instancias de las interfaces ID3DXFileEnumObject e ID3DXFileSaveObject y para registrar plantillas.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interfaz ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718297"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="bf4ab-103">Interfaz ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="bf4ab-103">ID3DXFile interface</span></span>

<span data-ttu-id="bf4ab-104">Las aplicaciones usan los métodos de la interfaz ID3DXFile para crear instancias de las interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) y para registrar plantillas.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="bf4ab-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf4ab-105">Members</span></span>

<span data-ttu-id="bf4ab-106">La interfaz **ID3DXFile** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bf4ab-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bf4ab-107">**ID3DXFile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf4ab-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="bf4ab-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf4ab-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bf4ab-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf4ab-109">Methods</span></span>

<span data-ttu-id="bf4ab-110">La interfaz **ID3DXFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="bf4ab-111">Método</span><span class="sxs-lookup"><span data-stu-id="bf4ab-111">Method</span></span>                                                            | <span data-ttu-id="bf4ab-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf4ab-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf4ab-113">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="bf4ab-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="bf4ab-114">Crea un objeto enumerador que leerá un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="bf4ab-115">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="bf4ab-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="bf4ab-116">Crea un objeto Save que se usará para guardar los datos en un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="bf4ab-117">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="bf4ab-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="bf4ab-118">Registra plantillas personalizadas, dado un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4ab-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="bf4ab-119">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="bf4ab-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="bf4ab-120">Registra plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="bf4ab-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf4ab-121">Remarks</span></span>

<span data-ttu-id="bf4ab-122">Un objeto ID3DXFile también contiene un almacén de plantillas local.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="bf4ab-123">Este almacenamiento local se puede Agregar solo a con los métodos [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) y [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4ab-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="bf4ab-124">Los objetos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) y [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) creados con [**ID3DXFile:: CreateEnumObject**](id3dxfile--createenumobject.md) y [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) también usan el almacén de plantillas del objeto primario ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="bf4ab-125">La interfaz ID3DXFile se obtiene mediante una llamada a la función [**D3DXFileCreate**](d3dxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4ab-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="bf4ab-126">El identificador único global (GUID) de la interfaz ID3DXFile es IID \_ ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="bf4ab-127">El tipo LPD3DXFILE se define como un puntero a la interfaz ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="bf4ab-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="bf4ab-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4ab-128">Requirements</span></span>



| <span data-ttu-id="bf4ab-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4ab-129">Requirement</span></span> | <span data-ttu-id="bf4ab-130">Value</span><span class="sxs-lookup"><span data-stu-id="bf4ab-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4ab-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf4ab-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bf4ab-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf4ab-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="bf4ab-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf4ab-133">Library</span></span><br/> | <dl> <span data-ttu-id="bf4ab-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf4ab-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bf4ab-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf4ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf4ab-136">Interfaces de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="bf4ab-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
