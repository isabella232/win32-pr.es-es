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
# <a name="xml-canonicalization"></a>Canonización XML

La canonización XML resuelve el problema de convertir un conjunto de nodos XML en bytes de tal forma que los cambios triviales en el XML (como cambiar el orden de los atributos de un elemento) no cambian el formato de bytes resultante. Los bytes obtenidos de la canonización se suelen usar para generar una firma criptográfica sobre el contenido XML.


Los algoritmos de canonización XML usados comúnmente normalizan los aspectos siguientes:

-   Codificación de caracteres (UTF-8 sin preámbulo)
-   Avance de alimentación y otros formatos de caracteres
-   Orden de los atributos en un elemento
-   Formulario de elemento vacío
-   Representar declaraciones de espacios de nombres

Las API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) y [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) proporcionan la funcionalidad de canonización XML al leer un documento.

Las API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) y [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) proporcionan la funcionalidad de canonización XML mientras se escribe un documento.

Las enumeraciones siguientes se usan con la canonización:

-   [**\_algoritmo de \_ canonización de WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**identificador de la \_ \_ propiedad de canonización de WS XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Las siguientes funciones se usan con la canonización:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Las siguientes estructuras se usan con la canonización:

-   [**\_ \_ \_ prefijos inclusivos de canonización de WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**\_propiedad de \_ canonización de XML de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




