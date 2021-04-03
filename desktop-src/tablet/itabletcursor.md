---
description: Representa un objeto de lápiz óptico.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interfaz ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913301"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="550a6-103">Interfaz ITabletCursor</span><span class="sxs-lookup"><span data-stu-id="550a6-103">ITabletCursor interface</span></span>

<span data-ttu-id="550a6-104">Representa un objeto de lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="550a6-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="550a6-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="550a6-105">Members</span></span>

<span data-ttu-id="550a6-106">La interfaz **ITabletCursor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="550a6-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="550a6-107">**ITabletCursor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="550a6-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="550a6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="550a6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="550a6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="550a6-109">Methods</span></span>

<span data-ttu-id="550a6-110">La interfaz **ITabletCursor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="550a6-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="550a6-111">Método</span><span class="sxs-lookup"><span data-stu-id="550a6-111">Method</span></span>                                                 | <span data-ttu-id="550a6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="550a6-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="550a6-113">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="550a6-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="550a6-114">Recupera el objeto de botón especificado de un lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="550a6-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="550a6-115">**GetButtonCount**</span><span class="sxs-lookup"><span data-stu-id="550a6-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="550a6-116">Recupera el número de botones del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="550a6-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="550a6-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="550a6-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="550a6-118">Recupera el identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="550a6-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="550a6-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="550a6-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="550a6-120">Recupera el nombre del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="550a6-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="550a6-121">**IsInverted**</span><span class="sxs-lookup"><span data-stu-id="550a6-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="550a6-122">Indica si el lápiz está en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="550a6-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="550a6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="550a6-123">Remarks</span></span>

<span data-ttu-id="550a6-124">No utilice esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="550a6-124">Do not use this interface.</span></span>

<span data-ttu-id="550a6-125">En el código siguiente se describe cómo se define la interfaz **ITabletCursor** .</span><span class="sxs-lookup"><span data-stu-id="550a6-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="550a6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="550a6-126">Requirements</span></span>



| <span data-ttu-id="550a6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="550a6-127">Requirement</span></span> | <span data-ttu-id="550a6-128">Value</span><span class="sxs-lookup"><span data-stu-id="550a6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="550a6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="550a6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="550a6-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="550a6-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="550a6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="550a6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="550a6-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="550a6-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="550a6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="550a6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="550a6-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="550a6-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

