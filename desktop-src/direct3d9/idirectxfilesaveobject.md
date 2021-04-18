---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileSaveObject para crear objetos de datos y para guardar plantillas y objetos de datos.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interfaz IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717719"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="95a8f-103">Interfaz IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="95a8f-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="95a8f-104">Las aplicaciones usan los métodos de la interfaz IDirectXFileSaveObject para crear objetos de datos y para guardar plantillas y objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="95a8f-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="95a8f-105">Tenga en cuenta que no se requieren plantillas en todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="95a8f-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="95a8f-106">Por ejemplo, puede colocar todas las plantillas en un solo archivo de Microsoft DirectX, en lugar de duplicarlas en cada archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="95a8f-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="95a8f-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="95a8f-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="95a8f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="95a8f-108">Members</span></span>

<span data-ttu-id="95a8f-109">La interfaz **IDirectXFileSaveObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="95a8f-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95a8f-110">**IDirectXFileSaveObject** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95a8f-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="95a8f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="95a8f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95a8f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="95a8f-112">Methods</span></span>

<span data-ttu-id="95a8f-113">La interfaz **IDirectXFileSaveObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="95a8f-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="95a8f-114">Método</span><span class="sxs-lookup"><span data-stu-id="95a8f-114">Method</span></span>                                                               | <span data-ttu-id="95a8f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="95a8f-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="95a8f-116">**CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="95a8f-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="95a8f-117">Crea un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="95a8f-117">Creates a data object.</span></span> <span data-ttu-id="95a8f-118">En desuso.</span><span class="sxs-lookup"><span data-stu-id="95a8f-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="95a8f-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="95a8f-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="95a8f-120">Guarda un objeto de datos y sus elementos secundarios en un archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="95a8f-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="95a8f-121">En desuso.</span><span class="sxs-lookup"><span data-stu-id="95a8f-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="95a8f-122">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="95a8f-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="95a8f-123">Guarda las plantillas en un archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="95a8f-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="95a8f-124">En desuso.</span><span class="sxs-lookup"><span data-stu-id="95a8f-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="95a8f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95a8f-125">Remarks</span></span>

<span data-ttu-id="95a8f-126">El identificador único global (GUID) de la interfaz IDirectXFileSaveObject es **IID \_ IDirectXFileSaveObject**.</span><span class="sxs-lookup"><span data-stu-id="95a8f-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="95a8f-127">La interfaz **IDirectXFileSaveObject** se obtiene llamando al método [**IDirectXFile:: CreateSaveObject**](idirectxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="95a8f-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="95a8f-128">El tipo **LPDIRECTXFILESAVEOBJECT** se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="95a8f-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="95a8f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a8f-129">Requirements</span></span>



| <span data-ttu-id="95a8f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a8f-130">Requirement</span></span> | <span data-ttu-id="95a8f-131">Value</span><span class="sxs-lookup"><span data-stu-id="95a8f-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95a8f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95a8f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="95a8f-133"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a8f-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="95a8f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95a8f-134">Library</span></span><br/> | <dl> <span data-ttu-id="95a8f-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95a8f-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a8f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="95a8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a8f-137">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="95a8f-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
