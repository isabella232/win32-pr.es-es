---
title: Identificadores de cliente
description: Identificadores de cliente
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Text Services Framework (TSF), identificadores de cliente
- TSF (marco de trabajo de servicios de texto), identificadores de cliente
- servicios de texto, identificadores de cliente
- Aplicaciones habilitadas para TSF, identificadores de cliente
- identificadores de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994045"
---
# <a name="client-identifiers"></a><span data-ttu-id="bbca5-108">Identificadores de cliente</span><span class="sxs-lookup"><span data-stu-id="bbca5-108">Client Identifiers</span></span>

## <a name="applications"></a><span data-ttu-id="bbca5-109">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="bbca5-109">Applications</span></span>

<span data-ttu-id="bbca5-110">Una aplicación obtiene su identificador de cliente mediante una llamada a [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="bbca5-110">An application obtains its client identifier by calling [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span>

## <a name="text-services"></a><span data-ttu-id="bbca5-111">Servicios de texto</span><span class="sxs-lookup"><span data-stu-id="bbca5-111">Text Services</span></span>

<span data-ttu-id="bbca5-112">Un servicio de texto obtiene su identificador de cliente cuando se llama al método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="bbca5-112">A text service obtains its client identifier when the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method is called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbca5-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbca5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbca5-114">ITfThreadMgr:: Activate</span><span class="sxs-lookup"><span data-stu-id="bbca5-114">ITfThreadMgr::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[<span data-ttu-id="bbca5-115">ITfTextInputProcessor:: Activate</span><span class="sxs-lookup"><span data-stu-id="bbca5-115">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




