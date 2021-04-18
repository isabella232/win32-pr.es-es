---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Qué es un documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707607"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Qué es un documento de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Merece la pena enumerar parte de la funcionalidad y la información que el documento de PrintCapabilities no debe proporcionar.

Un documento de PrintCapabilities:

-   No representa datos multivalor (dependiente de la configuración).

    Cada documento de PrintCapabilities se construye para una configuración específica. Ninguna propiedad o ScoredProperty del documento puede tener un valor que dependa de la configuración determinada. En la versión de esquema inicial, el proveedor de PrintCapabilities debe procesar el PrintTicket de entrada y crear un documento de PrintCapabilities que contenga los valores de propiedad adecuados para la configuración especificada en el PrintTicket.

-   No contiene información de restricciones.

    El documento de PrintCapabilities no indica qué configuraciones están permitidas y cuáles no. En la versión de esquema inicial, el proveedor de PrintCapabilities debe almacenar toda la información necesaria para validar las configuraciones, proporcionar un método que valide el PrintTicket de entrada y devolver un PrintTicket corregido en caso de que el PrintTicket especificado infrinja una o más restricciones.

-   No contiene información dinámica del dispositivo.

    Hay demasiada sobrecarga en la creación del documento de PrintCapabilities para que se utilice para mantener la información de estado cambiante, como los niveles de tinta, el papel restante en cada bandeja o el estado del atasco de papel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



