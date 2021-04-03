---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFile para crear instancias de las interfaces IDirectXFileEnumObject e IDirectXFileSaveObject y para registrar plantillas. En desuso.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interfaz IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914794"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="5a087-104">Interfaz IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="5a087-104">IDirectXFile interface</span></span>

<span data-ttu-id="5a087-105">Las aplicaciones usan los métodos de la interfaz IDirectXFile para crear instancias de las interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) y para registrar plantillas.</span><span class="sxs-lookup"><span data-stu-id="5a087-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="5a087-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="5a087-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="5a087-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a087-107">Members</span></span>

<span data-ttu-id="5a087-108">La interfaz **IDirectXFile** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5a087-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5a087-109">**IDirectXFile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a087-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="5a087-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a087-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a087-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a087-111">Methods</span></span>

<span data-ttu-id="5a087-112">La interfaz **IDirectXFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5a087-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="5a087-113">Método</span><span class="sxs-lookup"><span data-stu-id="5a087-113">Method</span></span>                                                       | <span data-ttu-id="5a087-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a087-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="5a087-115">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="5a087-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="5a087-116">Crea un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="5a087-116">Creates an enumerator object.</span></span> <span data-ttu-id="5a087-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="5a087-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="5a087-118">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="5a087-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="5a087-119">Crea un objeto Save.</span><span class="sxs-lookup"><span data-stu-id="5a087-119">Creates a save object.</span></span> <span data-ttu-id="5a087-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="5a087-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="5a087-121">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="5a087-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="5a087-122">Registra plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5a087-122">Registers custom templates.</span></span> <span data-ttu-id="5a087-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="5a087-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="5a087-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a087-124">Remarks</span></span>

<span data-ttu-id="5a087-125">El identificador único global (GUID) de la interfaz IDirectXFile es IID \_ IDirectXFile.</span><span class="sxs-lookup"><span data-stu-id="5a087-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="5a087-126">La interfaz IDirectXFile se obtiene mediante una llamada a la función [**DirectXFileCreate**](directxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="5a087-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="5a087-127">El tipo LPDIRECTXFILE se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="5a087-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="5a087-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a087-128">Requirements</span></span>



| <span data-ttu-id="5a087-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a087-129">Requirement</span></span> | <span data-ttu-id="5a087-130">Value</span><span class="sxs-lookup"><span data-stu-id="5a087-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a087-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a087-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5a087-132"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a087-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a087-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a087-133">Library</span></span><br/> | <dl> <span data-ttu-id="5a087-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a087-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a087-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a087-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a087-136">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="5a087-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
