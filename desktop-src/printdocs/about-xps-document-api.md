---
description: La API de documentos XPS implementa el modelo de objetos XPS y permite a los desarrolladores crear un OM XPS, manipular el contenido de un documento XPS en programas nativos de Windows \\ \\ y guardar el OM XPS en un archivo o una secuencia como un documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Acerca de la API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697516"
---
# <a name="about-xps-document-api"></a>Acerca de la API de documento XPS

La [API de documentos XPS](documents-xps.md) implementa el modelo de objetos XPS y permite a los desarrolladores crear un OM XPS, manipular el contenido de un documento XPS en programas nativos de Windows \\ \\ y guardar el OM XPS en un archivo o una secuencia como un documento XPS. Los desarrolladores de módulos de canalización de filtros XPSDrv también pueden usar la API de documentos XPS para manipular el contenido de un documento XPS en un filtro de controlador de impresora XPSDrv.

## <a name="xps-document-api-overview"></a>Introducción a la API de documento XPS

El modelo de objetos XPS es el modelo de información de un documento XPS. El modelo de información del documento XPS es independiente del modelo de marcado que se utiliza dentro de los elementos del documento. El modelo de objetos XPS describe la organización de los componentes internos que componen un documento XPS y el modelo de marcado describe el contenido de esos componentes.

En un programa, se crea una instancia del modelo de objetos XPS como un OM XPS. El OM XPS es esencialmente una versión en memoria del contenido de un documento XPS. Aunque es similar en una organización lógica a un documento XPS, un OM XPS no se considera un documento XPS hasta que se ha serializado a un archivo o una secuencia.

La estructura exacta del marcado no está disponible para el modelo de objetos XPS cuando se deserializa un documento XPS del marcado a un OM XPS. Por ejemplo, si la propiedad se representara como un elemento o un atributo en el marcado, el OM XPS presenta el valor de la propiedad de un objeto de documento exactamente de la misma manera.

La [API de documento XPS](documents-xps.md) se puede dividir en las siguientes categorías:

-   [Interfaces troncales de XPS OM](xps-om-trunk-interfaces.md)

    Las interfaces de tronco proporcionan acceso a los componentes de nivel superior de la estructura del documento XPS. Estas interfaces también proporcionan los medios para serializar un modelo de objetos XPS y deserializar un documento XPS.

-   [Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)

    Las interfaces de página proporcionan acceso al contenido de una página en un documento XPS. Las interfaces que describen el contenido de la página también se incluyen con las interfaces de página.

-   [Firmas digitales de XPS OM](using-the-xps-digital-signatures.md)

    El modelo de objetos de XPS admite firmas digitales. Sin embargo, puede tener acceso a las firmas digitales en un documento XPS directamente sin crear un OM XPS. Para obtener más información sobre cómo acceder a las firmas digitales XPS sin un OM XPS, consulte la [API de firma digital XPS](xps-digital-signatures.md).

-   [Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)

    Los documentos XPS admiten la impresión de vales en el nivel de paquete (trabajo), documento y página. Los vales de impresión contienen información sobre cómo dar formato al contenido del documento para imprimirlo o verlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**En esta sección**
</dt> <dt>

[Interfaces troncales de XPS OM](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfaces de página de XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Firmas digitales de XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfaces de vales de impresión de XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Otros temas relacionados**
</dt> <dt>

[Inicializar un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Firmas digitales de XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Referencia de la API de documentos XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



