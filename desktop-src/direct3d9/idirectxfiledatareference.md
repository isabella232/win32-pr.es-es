---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileDataReference para admitir objetos de referencia de datos.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interfaz IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157272"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="92ef2-103">Interfaz IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="92ef2-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="92ef2-104">Las aplicaciones usan los métodos de la interfaz IDirectXFileDataReference para admitir objetos de referencia de datos.</span><span class="sxs-lookup"><span data-stu-id="92ef2-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="92ef2-105">Un objeto de referencia de datos hace referencia a un objeto de datos que se ha definido anteriormente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="92ef2-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="92ef2-106">Esto le permite usar el mismo objeto varias veces sin repetirlo en el archivo.</span><span class="sxs-lookup"><span data-stu-id="92ef2-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="92ef2-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="92ef2-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="92ef2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="92ef2-108">Members</span></span>

<span data-ttu-id="92ef2-109">La interfaz **IDirectXFileDataReference** hereda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="92ef2-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="92ef2-110">**IDirectXFileDataReference** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="92ef2-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="92ef2-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="92ef2-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="92ef2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="92ef2-112">Methods</span></span>

<span data-ttu-id="92ef2-113">La interfaz **IDirectXFileDataReference** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="92ef2-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="92ef2-114">Método</span><span class="sxs-lookup"><span data-stu-id="92ef2-114">Method</span></span>                                                | <span data-ttu-id="92ef2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="92ef2-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="92ef2-116">**Resolver**</span><span class="sxs-lookup"><span data-stu-id="92ef2-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="92ef2-117">Resuelve referencias de datos.</span><span class="sxs-lookup"><span data-stu-id="92ef2-117">Resolves data references.</span></span> <span data-ttu-id="92ef2-118">En desuso.</span><span class="sxs-lookup"><span data-stu-id="92ef2-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92ef2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92ef2-119">Remarks</span></span>

<span data-ttu-id="92ef2-120">Una vez que haya determinado que un objeto es un objeto de referencia de datos, use el método [**IDirectXFileDataReference:: Resolve**](idirectxfiledatareference--resolve.md) para recuperar el objeto al que se hace referencia definido anteriormente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="92ef2-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="92ef2-121">Para obtener información sobre cómo identificar un objeto de referencia de datos, vea la interfaz [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="92ef2-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="92ef2-122">El GUID de la interfaz IDirectXFileDataReference es IID \_ IDirectXFileDataReference.</span><span class="sxs-lookup"><span data-stu-id="92ef2-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="92ef2-123">El tipo LPDIRECTXFILEDataReference se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="92ef2-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="92ef2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92ef2-124">Requirements</span></span>



| <span data-ttu-id="92ef2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92ef2-125">Requirement</span></span> | <span data-ttu-id="92ef2-126">Value</span><span class="sxs-lookup"><span data-stu-id="92ef2-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92ef2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92ef2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="92ef2-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ef2-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="92ef2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92ef2-129">Library</span></span><br/> | <dl> <span data-ttu-id="92ef2-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92ef2-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ef2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="92ef2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ef2-132">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="92ef2-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="92ef2-133">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="92ef2-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




