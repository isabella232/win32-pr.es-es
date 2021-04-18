---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interfaz IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718386"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="935a8-103">Interfaz IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="935a8-103">IDirectXFileData interface</span></span>

<span data-ttu-id="935a8-104">Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="935a8-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="935a8-105">Las restricciones de las plantillas determinan la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="935a8-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="935a8-106">Los tipos de datos permitidos por la plantilla se denominan miembros opcionales.</span><span class="sxs-lookup"><span data-stu-id="935a8-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="935a8-107">Los miembros opcionales no son necesarios, pero es posible que un objeto pierda información importante sin ellos.</span><span class="sxs-lookup"><span data-stu-id="935a8-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="935a8-108">Estos miembros opcionales se guardan como elementos secundarios del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="935a8-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="935a8-109">Los elementos secundarios pueden ser otro objeto de datos, una referencia a un objeto de datos anterior o un objeto binario.</span><span class="sxs-lookup"><span data-stu-id="935a8-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="935a8-110">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="935a8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="935a8-111">Members</span></span>

<span data-ttu-id="935a8-112">La interfaz **IDirectXFileData** hereda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="935a8-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="935a8-113">**IDirectXFileData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="935a8-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="935a8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="935a8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="935a8-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="935a8-115">Methods</span></span>

<span data-ttu-id="935a8-116">La interfaz **IDirectXFileData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="935a8-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="935a8-117">Método</span><span class="sxs-lookup"><span data-stu-id="935a8-117">Method</span></span>                                                         | <span data-ttu-id="935a8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="935a8-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="935a8-119">**AddBinaryObject**</span><span class="sxs-lookup"><span data-stu-id="935a8-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="935a8-120">Crea un objeto binario y lo agrega como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="935a8-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="935a8-121">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="935a8-122">**AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="935a8-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="935a8-123">Agrega un objeto de datos como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="935a8-123">Adds a data object as a child object.</span></span> <span data-ttu-id="935a8-124">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="935a8-125">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="935a8-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="935a8-126">Crea y agrega un objeto de referencia de datos como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="935a8-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="935a8-127">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="935a8-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="935a8-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="935a8-129">Recupera los datos para uno de los miembros del objeto o los datos de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="935a8-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="935a8-130">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="935a8-131">**GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="935a8-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="935a8-132">Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario del archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="935a8-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="935a8-133">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="935a8-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="935a8-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="935a8-135">Recupera el GUID de la plantilla del objeto.</span><span class="sxs-lookup"><span data-stu-id="935a8-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="935a8-136">En desuso.</span><span class="sxs-lookup"><span data-stu-id="935a8-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="935a8-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="935a8-137">Remarks</span></span>

<span data-ttu-id="935a8-138">El GUID de la interfaz IDirectXFileData es IID \_ IDirectXFileData.</span><span class="sxs-lookup"><span data-stu-id="935a8-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="935a8-139">El tipo LPDIRECTXFILEDATA se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="935a8-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="935a8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="935a8-140">Requirements</span></span>



| <span data-ttu-id="935a8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="935a8-141">Requirement</span></span> | <span data-ttu-id="935a8-142">Value</span><span class="sxs-lookup"><span data-stu-id="935a8-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="935a8-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="935a8-143">Header</span></span><br/>  | <dl> <span data-ttu-id="935a8-144"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="935a8-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="935a8-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="935a8-145">Library</span></span><br/> | <dl> <span data-ttu-id="935a8-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="935a8-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935a8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="935a8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935a8-148">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="935a8-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="935a8-149">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="935a8-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




