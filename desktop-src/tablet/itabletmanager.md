---
description: Proporciona acceso a todas las tabletas conectadas al equipo.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interfaz ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083404"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="2ee2c-103">Interfaz ITabletManager</span><span class="sxs-lookup"><span data-stu-id="2ee2c-103">ITabletManager interface</span></span>

<span data-ttu-id="2ee2c-104">Proporciona acceso a todas las tabletas conectadas al equipo.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="2ee2c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ee2c-105">Members</span></span>

<span data-ttu-id="2ee2c-106">La interfaz **ITabletManager** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2ee2c-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2ee2c-107">**ITabletManager** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2ee2c-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="2ee2c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ee2c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ee2c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ee2c-109">Methods</span></span>

<span data-ttu-id="2ee2c-110">La interfaz **ITabletManager** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="2ee2c-111">Método</span><span class="sxs-lookup"><span data-stu-id="2ee2c-111">Method</span></span>                                                  | <span data-ttu-id="2ee2c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ee2c-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="2ee2c-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ee2c-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="2ee2c-114">Recupera el objeto de tableta especificado.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="2ee2c-115">**GetTabletCount**</span><span class="sxs-lookup"><span data-stu-id="2ee2c-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="2ee2c-116">Recupera el número de tabletas conectadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ee2c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ee2c-117">Remarks</span></span>

<span data-ttu-id="2ee2c-118">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-118">Developers should not use this interface.</span></span>

<span data-ttu-id="2ee2c-119">En el código siguiente se muestra cómo se implementa la interfaz **ITabletManager** .</span><span class="sxs-lookup"><span data-stu-id="2ee2c-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="2ee2c-120">Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID. de clase de CLSID \_ TabletManagerS y, a continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero a la **interfaz ITabletManager**.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="2ee2c-121">El GUID de TabletManagerS de CLSID \_ se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2ee2c-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="2ee2c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee2c-122">Requirements</span></span>



| <span data-ttu-id="2ee2c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee2c-123">Requirement</span></span> | <span data-ttu-id="2ee2c-124">Value</span><span class="sxs-lookup"><span data-stu-id="2ee2c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee2c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee2c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee2c-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2ee2c-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2ee2c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee2c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee2c-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2ee2c-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2ee2c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ee2c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ee2c-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ee2c-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

