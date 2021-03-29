---
title: Compresión de secuencia
description: Compresión de secuencia
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Administrador de compresión de vídeo (VCM), compresión de secuencia
- VCM (Administrador de compresión de vídeo), compresión de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994176"
---
# <a name="sequence-compression"></a><span data-ttu-id="9c349-105">Compresión de secuencia</span><span class="sxs-lookup"><span data-stu-id="9c349-105">Sequence Compression</span></span>

<span data-ttu-id="9c349-106">La aplicación puede usar las funciones [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)y [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) para comprimir una secuencia de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9c349-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="9c349-107">Estas funciones utilizan los datos almacenados en la estructura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) .</span><span class="sxs-lookup"><span data-stu-id="9c349-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="9c349-108">Las aplicaciones usan la función [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para que el usuario pueda seleccionar un compresor, abrirlo y establecer los parámetros de compresión en la estructura **COMPVARS** . sin embargo, las aplicaciones pueden establecer los parámetros de la estructura manualmente.</span><span class="sxs-lookup"><span data-stu-id="9c349-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="9c349-109">Para que una aplicación pueda empezar a comprimir una secuencia de fotogramas, debe usar **ICSeqCompressFrameStart** para asignar los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9c349-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="9c349-110">Una vez asignados los recursos, la aplicación puede utilizar **ICSeqCompressFrame** para comprimir cada fotograma individualmente.</span><span class="sxs-lookup"><span data-stu-id="9c349-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="9c349-111">La velocidad de fotogramas y la frecuencia de fotogramas clave utilizada en la compresión de la secuencia se especifican en miembros de la estructura **COMPVARS** .</span><span class="sxs-lookup"><span data-stu-id="9c349-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="9c349-112">El valor devuelto para **ICSeqCompressFrame** apunta a los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="9c349-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="9c349-113">Cuando una aplicación termina de comprimir una secuencia, puede usar **ICSeqCompressFrameEnd** para liberar recursos del sistema asignados para **ICSeqCompressFrameStart**.</span><span class="sxs-lookup"><span data-stu-id="9c349-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="9c349-114">Para liberar los recursos asignados para la estructura **COMPVARS** , la aplicación puede usar la función [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .</span><span class="sxs-lookup"><span data-stu-id="9c349-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




