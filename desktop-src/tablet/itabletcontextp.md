---
description: Representa el contexto de la tableta.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interfaz ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717157"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="c6432-103">Interfaz ITabletContextP</span><span class="sxs-lookup"><span data-stu-id="c6432-103">ITabletContextP interface</span></span>

<span data-ttu-id="c6432-104">Representa el contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="c6432-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="c6432-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6432-105">Members</span></span>

<span data-ttu-id="c6432-106">La interfaz **ITabletContextP** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6432-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6432-107">**ITabletContextP** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6432-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="c6432-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6432-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6432-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6432-109">Methods</span></span>

<span data-ttu-id="c6432-110">La interfaz **ITabletContextP** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c6432-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="c6432-111">Método</span><span class="sxs-lookup"><span data-stu-id="c6432-111">Method</span></span>                                                                                           | <span data-ttu-id="c6432-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6432-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="c6432-113">**IsTopMostHook**</span><span class="sxs-lookup"><span data-stu-id="c6432-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="c6432-114">Indica si el contexto de la tableta está en el enlace más alto.</span><span class="sxs-lookup"><span data-stu-id="c6432-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="c6432-115">**Superpone**</span><span class="sxs-lookup"><span data-stu-id="c6432-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="c6432-116">Mueve un contexto de tableta al principio o al final de la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="c6432-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="c6432-117">**TrackInputRect**</span><span class="sxs-lookup"><span data-stu-id="c6432-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="c6432-118">Actualiza el digitalizador de Tablet PC a las coordenadas de asignación de ubicación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c6432-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="c6432-119">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="c6432-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="c6432-120">Proporciona acceso a la memoria compartida entre los subprocesos de tableta.</span><span class="sxs-lookup"><span data-stu-id="c6432-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="c6432-121">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="c6432-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="c6432-122">Proporciona acceso a la memoria compartida entre los subprocesos de tableta.</span><span class="sxs-lookup"><span data-stu-id="c6432-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c6432-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6432-123">Remarks</span></span>

<span data-ttu-id="c6432-124">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="c6432-124">Developers should not use this interface.</span></span>

<span data-ttu-id="c6432-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) solo está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c6432-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="c6432-126">En el código siguiente se describe cómo se define la interfaz **ITabletContextP** .</span><span class="sxs-lookup"><span data-stu-id="c6432-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="c6432-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6432-127">Requirements</span></span>



| <span data-ttu-id="c6432-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6432-128">Requirement</span></span> | <span data-ttu-id="c6432-129">Value</span><span class="sxs-lookup"><span data-stu-id="c6432-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6432-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6432-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c6432-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c6432-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c6432-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6432-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c6432-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c6432-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c6432-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6432-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6432-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6432-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

