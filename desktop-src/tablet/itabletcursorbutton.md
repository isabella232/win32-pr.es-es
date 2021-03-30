---
description: Representa información general sobre un botón en un dispositivo de lápiz óptico.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interfaz ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360972"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="dc1da-103">Interfaz ITabletCursorButton</span><span class="sxs-lookup"><span data-stu-id="dc1da-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="dc1da-104">Representa información general sobre un botón en un dispositivo de lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="dc1da-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="dc1da-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc1da-105">Members</span></span>

<span data-ttu-id="dc1da-106">La interfaz **ITabletCursorButton** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc1da-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc1da-107">**ITabletCursorButton** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc1da-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="dc1da-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc1da-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc1da-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc1da-109">Methods</span></span>

<span data-ttu-id="dc1da-110">La interfaz **ITabletCursorButton** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dc1da-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="dc1da-111">Método</span><span class="sxs-lookup"><span data-stu-id="dc1da-111">Method</span></span>                                         | <span data-ttu-id="dc1da-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc1da-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="dc1da-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="dc1da-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="dc1da-114">Recupera el identificador único del botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="dc1da-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="dc1da-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="dc1da-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="dc1da-116">Recupera el nombre del botón del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="dc1da-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="dc1da-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc1da-117">Remarks</span></span>

<span data-ttu-id="dc1da-118">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="dc1da-118">Developers should not use this interface.</span></span>

<span data-ttu-id="dc1da-119">En el código siguiente se muestra cómo se define la interfaz **ITabletCursorButton** .</span><span class="sxs-lookup"><span data-stu-id="dc1da-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="dc1da-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc1da-120">Requirements</span></span>



| <span data-ttu-id="dc1da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc1da-121">Requirement</span></span> | <span data-ttu-id="dc1da-122">Value</span><span class="sxs-lookup"><span data-stu-id="dc1da-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1da-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1da-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc1da-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dc1da-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1da-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc1da-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc1da-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc1da-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc1da-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc1da-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1da-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc1da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1da-130">**Interfaz ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="dc1da-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

