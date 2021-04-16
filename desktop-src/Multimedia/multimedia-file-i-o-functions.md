---
title: Funciones de e/s de archivos multimedia
description: Funciones de e/s de archivos multimedia
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Windows multimedia, funciones de e/s de archivos
- multimedia, funciones de e/s de archivos
- entrada multimedia, funciones de e/s de archivos
- e/s de archivos multimedia, funciones
- e/s de archivos, funciones
- entrada y salida (e/s), funciones
- E/s (entrada y salida), funciones
- referencia de e/s de archivos multimedia, funciones
- referencia de e/s de archivos multimedia, funciones
- referencia de e/s de archivo, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533112"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="9b3b9-113">Funciones de e/s de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="9b3b9-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="9b3b9-114">Las siguientes funciones se usan con e/s de archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="9b3b9-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="9b3b9-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b3b9-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="9b3b9-116">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="9b3b9-117">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="9b3b9-118">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="9b3b9-119">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="9b3b9-120">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="9b3b9-121">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="9b3b9-122">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="9b3b9-123">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="9b3b9-124">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="9b3b9-125">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="9b3b9-126">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="9b3b9-127">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="9b3b9-128">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="9b3b9-129">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="9b3b9-130">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="9b3b9-131">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="9b3b9-132">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="9b3b9-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="9b3b9-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b3b9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b3b9-134">Referencia de e/s de archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="9b3b9-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 