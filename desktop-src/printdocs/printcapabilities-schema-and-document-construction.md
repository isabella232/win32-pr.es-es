---
title: Esquemas y documentos de PrintCapabilities
description: El esquema PrintCapabilities está pensado para eliminar muchas de las limitaciones de las funciones de Win32 DevCaps.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21347fae1c9824df4a8355f8dd26de37eeac4604
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407078"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Esquema PrintCapabilities y construcción de documentos

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las funciones actuales de Win32 DevCaps (como GetDeviceCaps o DeviceCapabilities, que se describen en la documentación del Kit de desarrollo de software de plataforma (SDK) de Microsoft) limitan gravemente el tipo de información que pueden obtener los componentes que no son controladores, con respecto a las funcionalidades y propiedades de los dispositivos de impresión. No se admite la publicación de las funcionalidades de los procesadores de impresión ni existe un método para enumerar características no estándar. Por lo tanto, no hay ninguna manera de que un componente que no sea un controlador construya una interfaz de usuario completa. Además, el cliente o la aplicación no puede determinar completamente las funcionalidades de los dispositivos o las colas de impresión más allá de las proporcionadas por las funciones de Win32 DevCaps. Las funciones actuales no son extensibles, por lo que los dispositivos no pueden publicar nuevas propiedades o características.

El esquema PrintCapabilities está pensado para eliminar muchas de las limitaciones de las funciones de Win32 DevCaps al proporcionar un superconjunto de la funcionalidad que ofrecen estas funciones. Si se necesita más funcionalidad, un proveedor del documento PrintCapabilities puede ampliar las palabras clave de esquema de impresión, dentro de las restricciones de Print Schema Framework, mediante la adición de instancias de elementos definidas de forma privada. Debido a su dependencia de XML como medio de intercambio, cualquier consumidor de un documento PrintCapabilities puede acceder a todos los datos del documento sin restricciones y sin preocuparse por la compatibilidad con diferentes versiones del sistema operativo. En esta sección se describe el esquema PrintCapabilities y se detalla su uso.

La audiencia prevista para esta sección incluye los siguientes grupos:

-   Implementadores de la interfaz del proveedor PrintTicket/PrintCapabilities

-   Consumidores de PrintCapabilities

-   Clientes de la interfaz del proveedor PrintTicket/PrintCapabilities

La primera categoría de la lista anterior se conoce como proveedores de PrintCapabilities en el resto de esta sección. La segunda y la tercera categorías se conocen como consumidores de PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relación con el esquema de impresión y el esquema PrintTicket

Los esquemas PrintCapabilities y PrintTicket son partes especializadas del esquema de impresión. Las principales diferencias estructurales entre estos subconjuntos del esquema de impresión es que el esquema PrintCapabilities incluye instancias property y ParameterDef que no están contenidas en el esquema PrintTicket, mientras que el esquema PrintTicket contiene instancias property y ParameterInit que no están contenidas en el esquema PrintCapabilities. Excepto por estas diferencias, los esquemas PrintCapabilities e PrintTicket generalmente se reflejan entre sí en las instancias de contenido, uso compartido de características, opciones, scoredproperty y valores. Cualquier contenido compartido de este tipo debe mantenerse actualizado. Por ejemplo, si se realiza un cambio en la característica PageMediaSize del esquema PrintCapabilities, se debe realizar el mismo cambio en el esquema PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



