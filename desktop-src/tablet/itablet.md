---
description: Representa una tableta conectada al equipo.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interfaz ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720611"
---
# <a name="itablet-interface"></a><span data-ttu-id="468be-103">Interfaz ITablet</span><span class="sxs-lookup"><span data-stu-id="468be-103">ITablet interface</span></span>

<span data-ttu-id="468be-104">Representa una tableta conectada al equipo.</span><span class="sxs-lookup"><span data-stu-id="468be-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="468be-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="468be-105">Members</span></span>

<span data-ttu-id="468be-106">La interfaz **ITablet** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="468be-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="468be-107">**ITablet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="468be-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="468be-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="468be-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="468be-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="468be-109">Methods</span></span>

<span data-ttu-id="468be-110">La interfaz **ITablet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="468be-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="468be-111">Método</span><span class="sxs-lookup"><span data-stu-id="468be-111">Method</span></span>                                                                 | <span data-ttu-id="468be-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="468be-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="468be-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="468be-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="468be-114">Crea un objeto de contexto que describe el dispositivo de tableta especificado.</span><span class="sxs-lookup"><span data-stu-id="468be-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="468be-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="468be-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="468be-116">Recupera el objeto [**ITabletCursor**](itabletcursor.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="468be-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="468be-117">**GetCursorCount**</span><span class="sxs-lookup"><span data-stu-id="468be-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="468be-118">Recupera el número de objetos cursor asociados a la tableta.</span><span class="sxs-lookup"><span data-stu-id="468be-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="468be-119">**GetDefaultContextSettings**</span><span class="sxs-lookup"><span data-stu-id="468be-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="468be-120">Recupera los valores de contexto predeterminados para la tableta.</span><span class="sxs-lookup"><span data-stu-id="468be-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="468be-121">**GetHardwareCaps**</span><span class="sxs-lookup"><span data-stu-id="468be-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="468be-122">Recupera un valor que representa las funciones del hardware de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="468be-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="468be-123">**GetMaxInputRect**</span><span class="sxs-lookup"><span data-stu-id="468be-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="468be-124">Recupera un rectángulo que representa el área de entrada máxima de la tableta.</span><span class="sxs-lookup"><span data-stu-id="468be-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="468be-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="468be-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="468be-126">Recupera una cadena que contiene el nombre del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="468be-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="468be-127">**GetPlugAndPlayId**</span><span class="sxs-lookup"><span data-stu-id="468be-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="468be-128">Recupera una cadena que contiene el identificador de Plug and Play del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="468be-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="468be-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="468be-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="468be-130">Recupera los datos de métricas de una propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="468be-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="468be-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="468be-131">Remarks</span></span>

<span data-ttu-id="468be-132">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="468be-132">Developers should not use this interface.</span></span>

<span data-ttu-id="468be-133">En el código siguiente se describe cómo se define la interfaz **ITablet** .</span><span class="sxs-lookup"><span data-stu-id="468be-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="468be-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="468be-134">Requirements</span></span>



| <span data-ttu-id="468be-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="468be-135">Requirement</span></span> | <span data-ttu-id="468be-136">Value</span><span class="sxs-lookup"><span data-stu-id="468be-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="468be-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="468be-137">Minimum supported client</span></span><br/> | <span data-ttu-id="468be-138">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="468be-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="468be-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="468be-139">Minimum supported server</span></span><br/> | <span data-ttu-id="468be-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="468be-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="468be-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="468be-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="468be-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="468be-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

