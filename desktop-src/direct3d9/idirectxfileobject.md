---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileObject para recuperar información sobre los objetos de archivo de Microsoft DirectX. En desuso.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interfaz IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689874"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="cdcd8-104">Interfaz IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="cdcd8-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="cdcd8-105">Las aplicaciones usan los métodos de la interfaz IDirectXFileObject para recuperar información sobre los objetos de archivo de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="cdcd8-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="cdcd8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cdcd8-107">Members</span></span>

<span data-ttu-id="cdcd8-108">La interfaz **IDirectXFileObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cdcd8-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cdcd8-109">**IDirectXFileObject** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cdcd8-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="cdcd8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdcd8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cdcd8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdcd8-111">Methods</span></span>

<span data-ttu-id="cdcd8-112">La interfaz **IDirectXFileObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="cdcd8-113">Método</span><span class="sxs-lookup"><span data-stu-id="cdcd8-113">Method</span></span>                                         | <span data-ttu-id="cdcd8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdcd8-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdcd8-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="cdcd8-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="cdcd8-116">Recupera un puntero al GUID que identifica un objeto de archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="cdcd8-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="cdcd8-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="cdcd8-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="cdcd8-119">Recupera un puntero al nombre de un objeto de archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="cdcd8-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="cdcd8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdcd8-121">Remarks</span></span>

<span data-ttu-id="cdcd8-122">El GUID de la interfaz IDirectXFileObject es IID \_ IDirectXFileObject.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="cdcd8-123">El tipo LPDIRECTXFILEOBJECT se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="cdcd8-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="cdcd8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdcd8-124">Requirements</span></span>



| <span data-ttu-id="cdcd8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdcd8-125">Requirement</span></span> | <span data-ttu-id="cdcd8-126">Value</span><span class="sxs-lookup"><span data-stu-id="cdcd8-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcd8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdcd8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cdcd8-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdcd8-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdcd8-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdcd8-129">Library</span></span><br/> | <dl> <span data-ttu-id="cdcd8-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdcd8-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcd8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdcd8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcd8-132">Interfaces de archivo X</span><span class="sxs-lookup"><span data-stu-id="cdcd8-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
