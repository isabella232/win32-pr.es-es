---
title: Canonización XML
description: La canonización XML resuelve el problema de convertir un conjunto de nodos XML en bytes de tal forma que los cambios triviales en el XML (como cambiar el orden de los atributos de un elemento) no cambian el formato de bytes resultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Servicios Web de canonización XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904908"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="c8ed1-106">Canonización XML</span><span class="sxs-lookup"><span data-stu-id="c8ed1-106">XML Canonicalization</span></span>

<span data-ttu-id="c8ed1-107">La canonización XML resuelve el problema de convertir un conjunto de nodos XML en bytes de tal forma que los cambios triviales en el XML (como cambiar el orden de los atributos de un elemento) no cambian el formato de bytes resultante.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="c8ed1-108">Los bytes obtenidos de la canonización se suelen usar para generar una firma criptográfica sobre el contenido XML.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="c8ed1-109">Los algoritmos de canonización XML usados comúnmente normalizan los aspectos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="c8ed1-110">Codificación de caracteres (UTF-8 sin preámbulo)</span><span class="sxs-lookup"><span data-stu-id="c8ed1-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="c8ed1-111">Avance de alimentación y otros formatos de caracteres</span><span class="sxs-lookup"><span data-stu-id="c8ed1-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="c8ed1-112">Orden de los atributos en un elemento</span><span class="sxs-lookup"><span data-stu-id="c8ed1-112">Attribute order in an element</span></span>
-   <span data-ttu-id="c8ed1-113">Formulario de elemento vacío</span><span class="sxs-lookup"><span data-stu-id="c8ed1-113">Empty element form</span></span>
-   <span data-ttu-id="c8ed1-114">Representar declaraciones de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="c8ed1-114">Rendering namespace declarations</span></span>

<span data-ttu-id="c8ed1-115">Las API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) y [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) proporcionan la funcionalidad de canonización XML al leer un documento.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="c8ed1-116">Las API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) y [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) proporcionan la funcionalidad de canonización XML mientras se escribe un documento.</span><span class="sxs-lookup"><span data-stu-id="c8ed1-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="c8ed1-117">Las enumeraciones siguientes se usan con la canonización:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="c8ed1-118">**\_algoritmo de \_ canonización de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="c8ed1-119">**identificador de la \_ \_ propiedad de canonización de WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="c8ed1-120">Las siguientes funciones se usan con la canonización:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="c8ed1-121">**WsEndReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="c8ed1-122">**WsEndWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="c8ed1-123">**WsStartReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="c8ed1-124">**WsStartWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="c8ed1-125">Las siguientes estructuras se usan con la canonización:</span><span class="sxs-lookup"><span data-stu-id="c8ed1-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="c8ed1-126">**\_ \_ \_ prefijos inclusivos de canonización de WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="c8ed1-127">**\_propiedad de \_ canonización de XML de WS \_**</span><span class="sxs-lookup"><span data-stu-id="c8ed1-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




