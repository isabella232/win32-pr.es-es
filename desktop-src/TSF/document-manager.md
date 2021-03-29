---
title: Administrador de documentos
description: Administrador de documentos
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Marco de trabajo de servicios de texto (TSF), administrador de documentos
- TSF (marco de trabajo de servicios de texto), administrador de documentos
- servicios de texto, administrador de documentos
- Aplicaciones habilitadas para TSF, administrador de documentos
- Administrador de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774449"
---
# <a name="document-manager"></a><span data-ttu-id="fcf01-108">Administrador de documentos</span><span class="sxs-lookup"><span data-stu-id="fcf01-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="fcf01-109">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="fcf01-109">Applications</span></span>

<span data-ttu-id="fcf01-110">Para crear un objeto de administrador de documentos, una aplicación llama a [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span><span class="sxs-lookup"><span data-stu-id="fcf01-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="fcf01-111">La aplicación crea un objeto de administrador de documentos independiente para cada documento individual que mantiene la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fcf01-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="fcf01-112">La aplicación utiliza el administrador de documentos para crear contextos de edición, agregar un contexto a la pila de contexto y quitar un contexto de la pila de contexto.</span><span class="sxs-lookup"><span data-stu-id="fcf01-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="fcf01-113">Servicios de texto</span><span class="sxs-lookup"><span data-stu-id="fcf01-113">Text Services</span></span>

<span data-ttu-id="fcf01-114">Un servicio de texto nunca crea un objeto de administrador de documentos.</span><span class="sxs-lookup"><span data-stu-id="fcf01-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="fcf01-115">En su lugar, el servicio de texto obtiene el objeto actual del administrador de documentos mediante una llamada a [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span><span class="sxs-lookup"><span data-stu-id="fcf01-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="fcf01-116">Un servicio de texto utiliza el administrador de documentos para obtener el contexto en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="fcf01-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="fcf01-117">Un servicio de texto también puede usar el administrador de documentos para crear su propio contexto y agregarlo y quitarlo de la pila de contexto.</span><span class="sxs-lookup"><span data-stu-id="fcf01-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="fcf01-118">Normalmente, esto se hace cuando el servicio de texto debe mostrar alguna interfaz de usuario modal, como cuando se muestra una lista de palabras para permitir al usuario seleccionar una palabra.</span><span class="sxs-lookup"><span data-stu-id="fcf01-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="fcf01-119">Cuando se muestra la lista, el servicio de texto coloca su propio contexto en la pila.</span><span class="sxs-lookup"><span data-stu-id="fcf01-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="fcf01-120">Cuando se descarta la lista de palabras, el servicio de texto quita su contexto de la pila.</span><span class="sxs-lookup"><span data-stu-id="fcf01-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcf01-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcf01-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcf01-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="fcf01-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="fcf01-123">ITfThreadMgr::CreateDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="fcf01-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="fcf01-124">ITfThreadMgr::GetFocus</span><span class="sxs-lookup"><span data-stu-id="fcf01-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




