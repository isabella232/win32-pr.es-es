---
title: Esquemas y documentos de PrintCapabilities
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1b8e2827e451fd8b1df477c33fe18d6203d10c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721369"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Esquema y construcción de documentos de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las funciones DevCaps de Win32 actuales (como GetDeviceCaps o DeviceCapabilities, que se describen en la documentación del kit de desarrollo de software (SDK) de la plataforma Microsoft) limitan gravemente el tipo de información que los componentes que no son de controlador pueden obtener, con respecto a las capacidades y propiedades de los dispositivos de impresión. No se admite la publicación de las capacidades de los procesadores de impresión ni un método para enumerar características no estándar. Por lo tanto, no hay ninguna manera de que un componente que no sea un controlador construya una interfaz de usuario completa. Además, el cliente o la aplicación no puede determinar por completo las capacidades de los dispositivos o las colas de impresión más allá de las proporcionadas por las funciones DevCaps de Win32. Las funciones actuales no son extensibles, por lo que los dispositivos no pueden publicar nuevas propiedades o características.

El esquema de PrintCapabilities está diseñado para eliminar muchas de las limitaciones de las funciones de DevCaps de Win32 proporcionando un supraconjunto de la funcionalidad que ofrecen estas funciones. Si se necesita más funcionalidad, un proveedor del documento de PrintCapabilities puede extender las palabras clave del esquema de impresión, dentro de las restricciones del marco de trabajo del esquema de impresión, agregando instancias de elemento definidas de forma privada. Debido a su dependencia de XML como medio de intercambio, cualquier consumidor de un documento de PrintCapabilities puede tener acceso a todos los datos del documento sin restricciones y sin preocuparse por la compatibilidad con versiones diferentes del sistema operativo. En esta sección se describe el esquema de PrintCapabilities y los detalles de su uso.

El público previsto para esta sección incluye los siguientes grupos:

-   Implementadores de la interfaz del proveedor PrintTicket/PrintCapabilities

-   Consumidores de PrintCapabilities

-   Clientes de la interfaz del proveedor PrintTicket/PrintCapabilities

La primera categoría de la lista anterior se conoce como proveedores de PrintCapabilities en el resto de esta sección. La segunda y tercera categorías se conocen como consumidores de PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relación con el esquema de impresión y el esquema PrintTicket

Los esquemas de PrintCapabilities y PrintTicket son partes especializadas del esquema de impresión. Las principales diferencias estructurales entre estos subconjuntos del esquema de impresión es que el esquema de PrintCapabilities incluye instancias de Property y ParameterDef que no están contenidas en el esquema PrintTicket, mientras que el esquema PrintTicket contiene las instancias de Property y ParameterInit que no están contenidas en el esquema PrintCapabilities. A excepción de estas diferencias, los esquemas de PrintCapabilities y PrintTicket generalmente se reflejan en el contenido, la característica de uso compartido, la opción, la ScoredProperty y las instancias de valor. Cualquier contenido compartido de este tipo debe mantenerse actualizado. Por ejemplo, si se realiza un cambio en la característica PageMediaSize en el esquema de PrintCapabilities, se debe realizar el mismo cambio en el esquema PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



