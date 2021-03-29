---
title: Enumeración de formato de entrada
description: Enumeración de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- SDK de Windows Media Format, enumeraciones de formato de entrada
- Windows Media Format SDK, enumerar formatos de entrada
- Advanced Systems Format (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- Advanced Systems Format (ASF), enumerar formatos de entrada
- ASF (formato de sistemas avanzados), enumerar formatos de entrada
- enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487010"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="76a62-110">Enumeración de formato de entrada</span><span class="sxs-lookup"><span data-stu-id="76a62-110">Input Format Enumeration</span></span>

<span data-ttu-id="76a62-111">El objeto de escritor obtiene la información de formato de secuencia del perfil que le asigna.</span><span class="sxs-lookup"><span data-stu-id="76a62-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="76a62-112">La información de configuración de secuencia de un perfil proporciona al escritor toda la información que necesita sobre cómo se escriben los datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="76a62-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="76a62-113">El perfil no proporciona al escritor información sobre el formato de los ejemplos de entrada que proporciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76a62-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="76a62-114">Los formatos de entrada serán desconocidos únicamente para las secuencias comprimidas con uno de los códecs de Windows Media. las entradas de tipos de flujo arbitrarios son predecibles en función de la información del perfil.</span><span class="sxs-lookup"><span data-stu-id="76a62-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="76a62-115">El objeto de escritor puede comunicarse con el códec de una secuencia para determinar los tipos de entrada que se pueden utilizar.</span><span class="sxs-lookup"><span data-stu-id="76a62-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="76a62-116">Se proporcionan métodos para enumerar los posibles tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="76a62-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="76a62-117">Siempre debe buscar el tipo de entrada que coincida con los medios de entrada mediante la enumeración de los tipos admitidos en lugar de establecer las propiedades de los medios de entrada manualmente.</span><span class="sxs-lookup"><span data-stu-id="76a62-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="76a62-118">Para obtener más información, vea [para enumerar los formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="76a62-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76a62-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76a62-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76a62-120">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="76a62-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="76a62-121">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="76a62-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




