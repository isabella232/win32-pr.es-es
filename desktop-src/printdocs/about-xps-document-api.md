---
description: La API de documentos XPS implementa el modelo de objetos XPS y permite a los desarrolladores crear un XPS OM, manipular el contenido del documento XPS en programas Windows nativos y guardar xpS OM en un archivo o secuencia como un \\ \\ documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Acerca de LA API de documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468542"
---
# <a name="about-xps-document-api"></a>Acerca de LA API de documentos XPS

La API de documentos [XPS](documents-xps.md) implementa el modelo de objetos XPS y permite a los desarrolladores crear un XPS OM, manipular el contenido del documento XPS en programas nativos de Windows y guardar xpS OM en un archivo o secuencia como un \\ \\ documento XPS. Los desarrolladores de módulos de canalización de filtros XPSDrv también pueden usar LA API de documentos XPS para manipular el contenido del documento XPS en un filtro de controlador de impresora XPSDrv.

## <a name="xps-document-api-overview"></a>Introducción a la API de documentos XPS

El modelo de objetos XPS es el modelo de información de un documento XPS. El modelo de información del documento XPS es independiente del modelo de marcado que se usa dentro de las partes del documento. El modelo de objetos XPS describe la organización de los componentes internos que forma un documento XPS y el modelo de marcado describe el contenido de esos componentes.

En un programa, se crea una instancia del modelo de objetos XPS como XPS OM. XpS OM es básicamente una versión en memoria del contenido de un documento XPS. Aunque es similar en la organización lógica a un documento XPS, un XPS OM no se considera un documento XPS hasta que se ha serializado en un archivo o una secuencia.

La estructura exacta del marcado no está disponible para xps om cuando se deserializa un documento XPS del marcado a un OM XPS. Por ejemplo, si la propiedad se representó como un elemento o un atributo en el marcado, el XPS OM presenta el valor de propiedad de un objeto de documento exactamente de la misma manera.

La [API de documentos XPS](documents-xps.md) se puede dividir en las siguientes categorías:

-   [Interfaces de tronco de OM XPS](xps-om-trunk-interfaces.md)

    Las interfaces de tronco proporcionan acceso a los componentes de nivel superior de la estructura del documento XPS. Estas interfaces también proporcionan los medios para serializar un XPS OM y deserializar un documento XPS.

-   [Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)

    Las interfaces de página proporcionan acceso al contenido de una página en un documento XPS. Las interfaces que describen el contenido de la página también se incluyen con las interfaces de página.

-   [XPS OM Digital Signatures](using-the-xps-digital-signatures.md)

    XPS OM admite firmas digitales. Sin embargo, puede acceder a las firmas digitales en un documento XPS directamente sin crear una OM xpS. Para obtener más información sobre cómo acceder a las firmas digitales XPS sin XPS OM, consulte [XPS Digital Signature API](xps-digital-signatures.md).

-   [Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)

    Los documentos XPS admiten vales de impresión en el nivel de paquete (trabajo), documento y página. Los vales de impresión contienen información sobre cómo dar formato al contenido del documento para imprimirlo o verlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**En esta sección**
</dt> <dt>

[Interfaces de tronco de OM XPS](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[XPS OM Digital Signatures](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Otros temas relacionados**
</dt> <dt>

[Inicialización de una instancia de XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[XPS OM Digital Signatures](using-the-xps-digital-signatures.md)
</dt> <dt>

[Referencia de LA API del documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



