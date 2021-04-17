---
title: Elemento Reference (obsoleto)
description: Elemento Reference (obsoleto)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metaarchivos de Windows Media, elemento de referencia
- Metafiles, elemento Reference
- elemento Reference
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704716"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="6cbd8-106">Elemento Reference (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="6cbd8-106">reference Element (deprecated)</span></span>

<span data-ttu-id="6cbd8-107">En este tema se documenta una característica que ya no se usa en la versión actual de los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="6cbd8-108">El elemento **Reference** contiene una lista de referencias a direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="6cbd8-109">Cada elemento de la lista tiene el formato Ref *XX*  =  *URL*, donde *XX* es un entero y *URL* es la dirección URL de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="6cbd8-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="6cbd8-110">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6cbd8-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="6cbd8-111">Los enteros representados por *XX* deben estar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="6cbd8-112">Es decir, el entero de cada línea debe ser mayor que el entero de la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="6cbd8-113">Cuando un programa cliente Lee un elemento de referencia, intenta conectarse al archivo multimedia representado por la primera dirección URL de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="6cbd8-114">Si se produce un error, el programa cliente intenta conectarse al archivo representado por la siguiente dirección URL de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="6cbd8-115">El programa cliente continúa hacia abajo en la lista hasta que realiza una conexión correcta o alcanza el final de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="6cbd8-116">Tenga en cuenta que si el programa cliente realiza una conexión correcta, no lee ninguna de las direcciones URL siguientes en la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="6cbd8-117">**Código de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6cbd8-117">**Example Code**</span></span>

<span data-ttu-id="6cbd8-118">En el ejemplo siguiente, el programa cliente primero intentaba conectarse al archivo representado por la dirección URL de MMS.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="6cbd8-119">Si se produjo un error, el programa cliente intentará conectarse al archivo representado por la dirección URL http.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="6cbd8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cbd8-120">Remarks</span></span>

<span data-ttu-id="6cbd8-121">El formato de archivo ASF abarca una amplia variedad de tipos de medios, como audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="6cbd8-122">Los archivos ASF también usan varias extensiones de nombre de archivo diferentes, entre las que se incluyen. WMA y. wmv.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="6cbd8-123">Los enteros representados por *XX* deben estar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="6cbd8-124">Es decir, el entero de cada línea debe ser mayor que el entero de la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="6cbd8-125">Cuando un programa cliente Lee un elemento de referencia, intenta conectarse al archivo multimedia representado por la primera dirección URL de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="6cbd8-126">Si se produce un error, el programa cliente intenta conectarse al archivo representado por la siguiente dirección URL de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="6cbd8-127">El programa cliente continúa hacia abajo en la lista hasta que realiza una conexión correcta o alcanza el final de la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="6cbd8-128">Tenga en cuenta que si el programa cliente realiza una conexión correcta, no lee ninguna de las direcciones URL siguientes en la lista.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cbd8-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6cbd8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cbd8-130">**Versiones anteriores de los metaarchivos de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="6cbd8-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




