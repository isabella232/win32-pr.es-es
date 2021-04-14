---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: '\_evento WMT de EC \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK de Windows Media Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Administración de derechos digitales (DRM), EC_WMT_EVENT
- DRM (administración de derechos digitales), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (formato de sistemas avanzados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488747"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="c15a7-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="c15a7-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c15a7-111">Lo envía el SDK de Windows Media Format cuando una aplicación usa el filtro de lector ASF para reproducir archivos ASF protegidos por la administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="c15a7-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="c15a7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c15a7-112">Parameters</span></span>

<span data-ttu-id="c15a7-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c15a7-113">*lParam1*</span></span>

<span data-ttu-id="c15a7-114">Puede ser uno de los siguientes valores de estado de WMT \_ .</span><span class="sxs-lookup"><span data-stu-id="c15a7-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="c15a7-115">Mensaje de estado de WMT \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="c15a7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c15a7-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c15a7-117">\_sin \_ derechos de WMT</span><span class="sxs-lookup"><span data-stu-id="c15a7-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="c15a7-118">El archivo está protegido con DRM versión 1 y la aplicación no tiene derechos para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="c15a7-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="c15a7-119">\_licencia de adquisición de WMT \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="c15a7-120">Se ha completado el proceso de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="c15a7-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="c15a7-121">(Esto no significa necesariamente que se haya adquirido una licencia correctamente).</span><span class="sxs-lookup"><span data-stu-id="c15a7-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="c15a7-122">\_no hay \_ derechos de WMT \_ ex</span><span class="sxs-lookup"><span data-stu-id="c15a7-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="c15a7-123">El archivo está protegido con DRM versión 7 y la aplicación no tiene derechos para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="c15a7-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="c15a7-124">WMT \_ necesita la \_ individualización</span><span class="sxs-lookup"><span data-stu-id="c15a7-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="c15a7-125">La licencia permite que solo las aplicaciones individuales realicen la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="c15a7-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="c15a7-126">individual de WMT \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="c15a7-127">Ahora se está llevando a cabo el proceso de individualización o se ha completado.</span><span class="sxs-lookup"><span data-stu-id="c15a7-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="c15a7-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c15a7-128">*lParam2*</span></span>

<span data-ttu-id="c15a7-129">Puntero a una estructura de **\_ \_ \_ datos de evento WMT de AM** que contiene información sobre el evento en el puntero de miembro de **pdata** , así como un código de estado **HRESULT** enviado por el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="c15a7-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="c15a7-130">El valor de *lParam2* depende del valor de *lParam1*, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c15a7-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="c15a7-131">(Las estructuras "WM \_ " se definen en el SDK de Windows Media Format).</span><span class="sxs-lookup"><span data-stu-id="c15a7-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="c15a7-132">Si lParam1 es...</span><span class="sxs-lookup"><span data-stu-id="c15a7-132">If lParam1 is...</span></span>              | <span data-ttu-id="c15a7-133">AM \_ \_ datos de evento WMT \_ . pdata es...</span><span class="sxs-lookup"><span data-stu-id="c15a7-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c15a7-134">\_sin \_ derechos de WMT</span><span class="sxs-lookup"><span data-stu-id="c15a7-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="c15a7-135">Puntero a una cadena **WCHAR** que contiene una dirección URL de desafío.</span><span class="sxs-lookup"><span data-stu-id="c15a7-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="c15a7-136">\_licencia de adquisición de WMT \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="c15a7-137">Un puntero a una estructura de **datos de licencia de Get de WM \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="c15a7-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="c15a7-138">\_no hay \_ derechos de WMT \_ ex</span><span class="sxs-lookup"><span data-stu-id="c15a7-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="c15a7-139">Un puntero a una estructura de **datos de licencia de Get de WM \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="c15a7-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="c15a7-140">WMT \_ necesita la \_ individualización</span><span class="sxs-lookup"><span data-stu-id="c15a7-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="c15a7-141">NULL.</span><span class="sxs-lookup"><span data-stu-id="c15a7-141">NULL.</span></span>                                                       |
| <span data-ttu-id="c15a7-142">individual de WMT \_</span><span class="sxs-lookup"><span data-stu-id="c15a7-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="c15a7-143">Un puntero a una estructura de estado de la **\_ \_ individualización de WM** .</span><span class="sxs-lookup"><span data-stu-id="c15a7-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c15a7-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c15a7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c15a7-145">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="c15a7-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c15a7-146">**Referencia de QASF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="c15a7-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="c15a7-147">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="c15a7-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




