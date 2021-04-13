---
description: Solucionador de origen
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Solucionador de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360475"
---
# <a name="source-resolver"></a><span data-ttu-id="e5365-103">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="e5365-103">Source Resolver</span></span>

<span data-ttu-id="e5365-104">La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión.</span><span class="sxs-lookup"><span data-stu-id="e5365-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="e5365-105">La resolución del origen es la forma estándar que tienen las aplicaciones para crear los orígenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="e5365-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="e5365-106">Internamente, la resolución de origen usa objetos de *controlador* :</span><span class="sxs-lookup"><span data-stu-id="e5365-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="e5365-107">Los *controladores de esquema* toman una dirección URL y crean un origen de medios o un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e5365-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="e5365-108">Los *controladores de secuencias de bytes* toman una secuencia de bytes y crean un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="e5365-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="e5365-109">Puede implementar un controlador personalizado y agregarlo al registro.</span><span class="sxs-lookup"><span data-stu-id="e5365-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="e5365-110">Los controladores de esquema se registran mediante el esquema de direcciones URL y los controladores de secuencias de bytes se registran mediante la extensión de nombre de archivo o el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="e5365-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="e5365-111">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="e5365-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e5365-112">Usar el solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="e5365-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="e5365-113">Configuración de un origen de medios</span><span class="sxs-lookup"><span data-stu-id="e5365-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="e5365-114">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="e5365-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="e5365-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5365-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5365-116">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="e5365-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



