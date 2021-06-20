---
description: Obtenga información sobre el formato PrintTicket, que expresa información de configuración mediante el marco de esquema de impresión basado en XML.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Esquema PrintTicket y construcción de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5998aeb534bbbeb16681a4136cf33425a7eefad7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405438"
---
# <a name="printticket-schema-and-document-construction"></a>Esquema PrintTicket y construcción de documentos

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El método actual de especificar información de configuración del dispositivo mediante una estructura DEVMODE sufre varias limitaciones. En primer lugar, la estructura DEVMODE es una estructura binaria, que puede dar lugar a problemas de versiones diferentes. En segundo lugar, se divide en una parte pública no próxima y una parte privada a la que solo pueden acceder los controladores y solo después el controlador específico que la creó. El formato PrintTicket expresa la información de configuración mediante el marco de esquema de impresión basado en XML, lo que elimina estas deficiencias de la estructura DEVMODE.

El esquema PrintTicket aborda cada uno de los dos problemas que se mencionan. En primer lugar, el esquema PrintTicket es un archivo de texto basado en XML, por lo que se eliminan los problemas de extensibilidad y control de versiones. En segundo lugar, la información de configuración está disponible para todos los clientes, lo que significa que cualquier cliente o proveedor puede almacenar y recuperar cualquier información contenida en un PrintTicket. Las opciones se describen con la misma técnica que usan el marco de esquema de impresión y el documento PrintCapabilities derivado. Por esta razón, PrintTicket proporciona todas las posibles ventajas de portabilidad del modelo de definición de opción que se va a realizar. Vea [Marco de esquema de impresión](print-schema-framework.md) para obtener más información. La audiencia prevista para esta sección incluye los siguientes grupos:

-   Implementadores de una interfaz de proveedor PrintTicket/PrintCapabilities

-   Consumidores de PrintTicket

-   Clientes de una interfaz de proveedor PrintTicket/PrintCapabilities

Los miembros de la primera categoría de la lista anterior se conocen como proveedores PrintTicket en el resto de esta sección. Los miembros de las dos últimas categorías se conocen como consumidores de PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relación con el esquema de impresión y el esquema PrintCapabilities

Los esquemas PrintTicket e PrintCapabilities son partes especializadas del esquema de impresión. Las principales diferencias estructurales entre estos subconjuntos del esquema de impresión es que el esquema PrintTicket contiene instancias property y ParameterInit que no están contenidas en el esquema PrintCapabilities, mientras que el esquema PrintCapabilities incluye instancias property y ParameterDef que no están contenidas en el esquema PrintTicket. Excepto por estas diferencias, los esquemas PrintCapabilities e PrintTicket generalmente se reflejan entre sí en las instancias de contenido, uso compartido de características, opciones, scoredproperty y valores. Cualquier contenido compartido de este tipo debe mantenerse actualizado. Por ejemplo, si se realiza un cambio en la característica MediaSize del esquema PrintCapabilities, se debe realizar el mismo cambio en el esquema PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



