---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre los datos binarios. En desuso.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaz IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280282"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="7e7d5-104">Interfaz IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="7e7d5-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="7e7d5-105">Las aplicaciones usan los métodos de la interfaz IDirectXFileBinary para leer y recuperar información sobre los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="7e7d5-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="7e7d5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e7d5-107">Members</span></span>

<span data-ttu-id="7e7d5-108">La interfaz **IDirectXFileBinary** hereda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="7e7d5-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="7e7d5-109">**IDirectXFileBinary** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e7d5-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="7e7d5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e7d5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7e7d5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e7d5-111">Methods</span></span>

<span data-ttu-id="7e7d5-112">La interfaz **IDirectXFileBinary** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="7e7d5-113">Método</span><span class="sxs-lookup"><span data-stu-id="7e7d5-113">Method</span></span>                                                 | <span data-ttu-id="7e7d5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e7d5-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e7d5-115">**GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="7e7d5-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="7e7d5-116">Recupera el tipo de extensiones multipropósito de correo Internet (MIME) para los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="7e7d5-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="7e7d5-118">**GetSize (**</span><span class="sxs-lookup"><span data-stu-id="7e7d5-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="7e7d5-119">Recupera el tamaño de los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="7e7d5-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="7e7d5-121">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="7e7d5-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="7e7d5-122">Lee los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-122">Reads the binary data.</span></span> <span data-ttu-id="7e7d5-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="7e7d5-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7d5-124">Remarks</span></span>

<span data-ttu-id="7e7d5-125">El GUID de la interfaz IDirectXFileBinary es IID \_ IDirectXFileBinary.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="7e7d5-126">El tipo LPDIRECTXFileBinary se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="7e7d5-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="7e7d5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7d5-127">Requirements</span></span>



| <span data-ttu-id="7e7d5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7d5-128">Requirement</span></span> | <span data-ttu-id="7e7d5-129">Value</span><span class="sxs-lookup"><span data-stu-id="7e7d5-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7d5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e7d5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7e7d5-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e7d5-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e7d5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e7d5-132">Library</span></span><br/> | <dl> <span data-ttu-id="7e7d5-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e7d5-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7d5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7d5-135">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="7e7d5-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="7e7d5-136">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="7e7d5-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




