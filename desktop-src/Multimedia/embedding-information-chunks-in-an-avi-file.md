---
title: Incrustar fragmentos de información en un archivo AVI
description: Incrustar fragmentos de información en un archivo AVI
ms.assetid: 010c7b15-131a-47c8-9444-ee148bd351b0
keywords:
- Mensaje WM_CAP_FILE_SET_INFOCHUNK
- capFileSetInfoChunk (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fdcf601b51c7fd825a6e6ca2d592a2ad566c6f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651304"
---
# <a name="embedding-information-chunks-in-an-avi-file"></a><span data-ttu-id="36469-105">Incrustar fragmentos de información en un archivo AVI</span><span class="sxs-lookup"><span data-stu-id="36469-105">Embedding Information Chunks in an AVI File</span></span>

<span data-ttu-id="36469-106">Puede insertar fragmentos de información, como texto o datos personalizados, en un archivo AVI mediante el mensaje INFOCHUNK de [**Cap de WM \_ \_ \_ set \_**](wm-cap-file-set-infochunk.md) (o la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) ).</span><span class="sxs-lookup"><span data-stu-id="36469-106">You can insert information chunks, such as text or custom data, in an AVI file by using the [**WM\_CAP\_FILE\_SET\_INFOCHUNK**](wm-cap-file-set-infochunk.md) message (or the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro).</span></span> <span data-ttu-id="36469-107">También puede usar este mensaje para borrar fragmentos de información de un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="36469-107">You can also use this message to clear information chunks from an AVI file.</span></span>

 

 




