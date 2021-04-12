---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos. Las restricciones de las plantillas determinan la jerarquía.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interfaz ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280402"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="2d67e-104">Interfaz ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="2d67e-104">ID3DXFileData interface</span></span>

<span data-ttu-id="2d67e-105">Las aplicaciones usan los métodos de la interfaz ID3DXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="2d67e-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="2d67e-106">Las restricciones de las plantillas determinan la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="2d67e-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="2d67e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d67e-107">Members</span></span>

<span data-ttu-id="2d67e-108">La interfaz **ID3DXFileData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d67e-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d67e-109">**ID3DXFileData** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d67e-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="2d67e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d67e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d67e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d67e-111">Methods</span></span>

<span data-ttu-id="2d67e-112">La interfaz **ID3DXFileData** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2d67e-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="2d67e-113">Método</span><span class="sxs-lookup"><span data-stu-id="2d67e-113">Method</span></span>                                            | <span data-ttu-id="2d67e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d67e-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d67e-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="2d67e-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="2d67e-116">Recupera un objeto secundario en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="2d67e-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="2d67e-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="2d67e-118">Recupera el número de elementos secundarios de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="2d67e-119">**GetEnum**</span><span class="sxs-lookup"><span data-stu-id="2d67e-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="2d67e-120">Recupera el objeto de enumeración en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="2d67e-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="2d67e-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="2d67e-122">Recupera el GUID de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="2d67e-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="2d67e-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="2d67e-124">Recupera el nombre de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="2d67e-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="2d67e-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="2d67e-126">Recupera el identificador de plantilla en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2d67e-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="2d67e-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="2d67e-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="2d67e-128">Indica si este objeto de datos de archivo es un objeto de referencia que apunta a otro objeto de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="2d67e-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="2d67e-129">**Lock**</span><span class="sxs-lookup"><span data-stu-id="2d67e-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="2d67e-130">Obtiene acceso a los datos del archivo. x.</span><span class="sxs-lookup"><span data-stu-id="2d67e-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="2d67e-131">**Pulsa**</span><span class="sxs-lookup"><span data-stu-id="2d67e-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="2d67e-132">Finaliza la duración del puntero *ppData* devuelto por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="2d67e-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d67e-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d67e-133">Remarks</span></span>

<span data-ttu-id="2d67e-134">Los tipos de datos permitidos por la plantilla se denominan miembros opcionales.</span><span class="sxs-lookup"><span data-stu-id="2d67e-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="2d67e-135">Los miembros opcionales no son necesarios, pero es posible que un objeto pierda información importante sin ellos.</span><span class="sxs-lookup"><span data-stu-id="2d67e-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="2d67e-136">Estos miembros opcionales se guardan como elementos secundarios del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="2d67e-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="2d67e-137">Un elemento secundario puede ser otro objeto de datos o una referencia a un objeto de datos anterior.</span><span class="sxs-lookup"><span data-stu-id="2d67e-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="2d67e-138">El GUID de la interfaz ID3DXFileData es IID \_ ID3DXFileData.</span><span class="sxs-lookup"><span data-stu-id="2d67e-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="2d67e-139">El tipo LPD3DXFILEDATA se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2d67e-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="2d67e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d67e-140">Requirements</span></span>



| <span data-ttu-id="2d67e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d67e-141">Requirement</span></span> | <span data-ttu-id="2d67e-142">Value</span><span class="sxs-lookup"><span data-stu-id="2d67e-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d67e-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d67e-143">Header</span></span><br/>  | <dl> <span data-ttu-id="2d67e-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d67e-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="2d67e-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d67e-145">Library</span></span><br/> | <dl> <span data-ttu-id="2d67e-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d67e-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d67e-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d67e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d67e-148">Interfaces de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="2d67e-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
