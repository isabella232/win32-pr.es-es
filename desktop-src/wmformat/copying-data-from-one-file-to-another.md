---
title: Copiar datos de un archivo a otro
description: Copiar datos de un archivo a otro
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- SDK de Windows Media Format, copiar datos
- Advanced Systems Format (ASF), copiar datos
- ASF (formato de sistemas avanzados), copiar datos
- flujos, copiar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994521"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="3e5a2-107">Copiar datos de un archivo a otro</span><span class="sxs-lookup"><span data-stu-id="3e5a2-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="3e5a2-108">En el nivel más básico, la copia de una secuencia de un archivo ASF a otro es bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="3e5a2-109">Sin embargo, hay problemas que se deben tener en cuenta al trabajar con secuencias de varios archivos de entrada o al copiar secuencias que primero descomprima y vuelva a codificar.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="3e5a2-110">En las secciones siguientes se describe la copia de secuencias.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="3e5a2-111">Sección</span><span class="sxs-lookup"><span data-stu-id="3e5a2-111">Section</span></span>                                                                                              | <span data-ttu-id="3e5a2-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="3e5a2-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e5a2-113">Copiar secuencias sin descomprimir los datos</span><span class="sxs-lookup"><span data-stu-id="3e5a2-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="3e5a2-114">Describe cómo copiar secuencias mediante ejemplos comprimidos para conservar la calidad del contenido.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="3e5a2-115">Copiar secuencias mediante ejemplos descomprimidos</span><span class="sxs-lookup"><span data-stu-id="3e5a2-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="3e5a2-116">Describe las dificultades en la copia de secuencias mediante ejemplos descomprimidos.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="3e5a2-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e5a2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e5a2-118">**Objeto del administrador de perfiles**</span><span class="sxs-lookup"><span data-stu-id="3e5a2-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="3e5a2-119">**Objeto de configuración del flujo**</span><span class="sxs-lookup"><span data-stu-id="3e5a2-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="3e5a2-120">**Objeto del lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="3e5a2-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="3e5a2-121">**Objeto de Writer**</span><span class="sxs-lookup"><span data-stu-id="3e5a2-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




