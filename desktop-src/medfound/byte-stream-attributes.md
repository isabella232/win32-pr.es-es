---
description: Atributos de secuencia de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de secuencia de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696181"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="1d9f6-103">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="1d9f6-103">Byte Stream Attributes</span></span>

<span data-ttu-id="1d9f6-104">Los siguientes atributos se aplican a algunos flujos de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="1d9f6-105">Para averiguar si una secuencia de bytes admite atributos, consulte el objeto de flujo de bytes para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1d9f6-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="1d9f6-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="1d9f6-106">Attribute</span></span>                                                                                  | <span data-ttu-id="1d9f6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d9f6-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="1d9f6-108">**tipo de contenido de MF \_ BYTESTREAM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1d9f6-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="1d9f6-109">Especifica el tipo MIME de una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="1d9f6-110">**\_duración de BYTESTREAM MF \_**</span><span class="sxs-lookup"><span data-stu-id="1d9f6-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="1d9f6-111">Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="1d9f6-112">\_BYTESTREAM \_ \_ identificador URI de archivo IFO \_</span><span class="sxs-lookup"><span data-stu-id="1d9f6-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="1d9f6-113">Especifica la dirección URL de un archivo IFO asociado.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="1d9f6-114">**\_hora de \_ última \_ modificación \_ de MF BYTESTREAM**</span><span class="sxs-lookup"><span data-stu-id="1d9f6-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="1d9f6-115">Especifica cuándo se modificó por última vez una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="1d9f6-116">**nombre del origen de MF \_ BYTESTREAM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1d9f6-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="1d9f6-117">Especifica la dirección URL original de un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="1d9f6-118">Los siguientes atributos se aplican a los controladores de secuencias de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="1d9f6-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="1d9f6-119">Attribute</span></span>                                                                                    | <span data-ttu-id="1d9f6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d9f6-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d9f6-121">MF \_ BYTESTREAMHANDLER \_ acepta la \_ escritura de recursos compartidos \_</span><span class="sxs-lookup"><span data-stu-id="1d9f6-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="1d9f6-122">Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso lo escriba.</span><span class="sxs-lookup"><span data-stu-id="1d9f6-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1d9f6-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d9f6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d9f6-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="1d9f6-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="1d9f6-125">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d9f6-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



