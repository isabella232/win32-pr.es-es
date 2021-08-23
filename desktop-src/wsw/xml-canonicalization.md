---
title: Canonización XML
description: La canonización XML resuelve el problema de convertir un conjunto de nodos XML en bytes de forma que los cambios triviales en el XML (como cambiar el orden de los atributos de un elemento) no cambien el formato de bytes resultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Servicios web de canonización XML para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082989"
---
# <a name="xml-canonicalization"></a>Canonización XML

La canonización XML resuelve el problema de convertir un conjunto de nodos XML en bytes de forma que los cambios triviales en el XML (como cambiar el orden de los atributos de un elemento) no cambien el formato de bytes resultante. Los bytes obtenidos de la canonización se usan normalmente para generar una firma criptográfica sobre contenido XML.


Los algoritmos de canonización XML usados habitualmente estandarizan los siguientes aspectos:

-   Codificación de caracteres (UTF-8 sin preámbulo)
-   Linefeed y otros formularios de caracteres
-   Orden de atributo en un elemento
-   Formulario de elemento vacío
-   Representación de declaraciones de espacio de nombres

Las API [**WsStartReaderÓniconicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) y [**WsEndReaderNtenicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) proporcionan la funcionalidad de canonización XML al leer un documento.

Las API [**WsStartWriterÓniconicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) y [**WsEndWriterNtenicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) proporcionan la funcionalidad de canonización XML al escribir un documento.

Las enumeraciones siguientes se usan con canonización:

-   [**ALGORITMO DE CANONIZACIÓN DE WS \_ \_ \_ XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**WS \_ XML \_ CANONICALIZATION \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Las funciones siguientes se usan con canonización:

-   [**WsEndReaderNtenicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterNtenicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderÓniconicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterNtenicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Las estructuras siguientes se usan con canonización:

-   [**PREFIJOS \_ INCLUSIVOS \_ DE CANONIZACIÓN \_ XML \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**WS \_ XML \_ \_ CANONICALIZATION, PROPIEDAD**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




