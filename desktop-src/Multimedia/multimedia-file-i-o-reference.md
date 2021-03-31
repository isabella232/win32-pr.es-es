---
title: Referencia de e/s de archivos multimedia
description: Referencia de e/s de archivos multimedia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows multimedia, referencia de e/s de archivo
- multimedia, referencia de e/s de archivos
- entrada multimedia, referencia de e/s de archivo
- e/s de archivos multimedia, referencia
- e/s de archivo, referencia
- entrada y salida (e/s), referencia
- E/s (entrada y salida), referencia
- referencia de e/s de archivos multimedia, acerca de
- referencia de e/s de archivos multimedia, acerca de
- referencia de e/s de archivo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789765"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="2ae90-113">Referencia de e/s de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="2ae90-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="2ae90-114">En esta sección se describen las funciones, macros, mensajes y estructuras asociadas a la entrada y salida de archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="2ae90-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="2ae90-115">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="2ae90-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="2ae90-116">E/s básicas</span><span class="sxs-lookup"><span data-stu-id="2ae90-116">Basic I/O</span></span>

-   [<span data-ttu-id="2ae90-117">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="2ae90-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="2ae90-118">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="2ae90-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="2ae90-119">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="2ae90-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="2ae90-120">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="2ae90-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="2ae90-121">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="2ae90-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="2ae90-122">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="2ae90-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="2ae90-123">E/s almacenada en búfer</span><span class="sxs-lookup"><span data-stu-id="2ae90-123">Buffered I/O</span></span>

-   [<span data-ttu-id="2ae90-124">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="2ae90-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="2ae90-125">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="2ae90-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="2ae90-126">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2ae90-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="2ae90-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ae90-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="2ae90-128">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ae90-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="2ae90-129">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2ae90-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="2ae90-130">RIFF E/S</span><span class="sxs-lookup"><span data-stu-id="2ae90-130">RIFF I/O</span></span>

-   [<span data-ttu-id="2ae90-131">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="2ae90-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="2ae90-132">**MMCKINFO**</span><span class="sxs-lookup"><span data-stu-id="2ae90-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="2ae90-133">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="2ae90-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="2ae90-134">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="2ae90-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="2ae90-135">**mmioFOURCC**</span><span class="sxs-lookup"><span data-stu-id="2ae90-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="2ae90-136">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="2ae90-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="2ae90-137">Procedimientos de e/s personalizados</span><span class="sxs-lookup"><span data-stu-id="2ae90-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="2ae90-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ae90-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="2ae90-139">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="2ae90-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="2ae90-140">**MMIOM \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="2ae90-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="2ae90-141">**MMIOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="2ae90-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="2ae90-142">**MMIOM \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="2ae90-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="2ae90-143">**MMIOM \_ cambiar nombre**</span><span class="sxs-lookup"><span data-stu-id="2ae90-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="2ae90-144">**búsqueda de MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="2ae90-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="2ae90-145">**escritura de MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="2ae90-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="2ae90-146">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="2ae90-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="2ae90-147">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="2ae90-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="2ae90-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ae90-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae90-149">E/s de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="2ae90-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 