---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Esquema PrintTicket y construcción de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe386638a7f119c52982f1911d602691455343f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279881"
---
# <a name="printticket-schema-and-document-construction"></a>Esquema PrintTicket y construcción de documentos

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El método actual de especificar la información de configuración de dispositivos mediante una estructura DEVMODE se ve afectado por varias limitaciones. En primer lugar, la estructura DEVMODE es una estructura binaria, lo que puede provocar problemas de versiones diferentes. En segundo lugar, se divide en una parte pública de nonextensible (y una parte privada a la que solo pueden acceder los controladores y, a continuación, el controlador específico que la creó. El formato PrintTicket expresa información de configuración mediante el marco de esquema de impresión basado en XML, con lo que se eliminan estas deficiencias de la estructura DEVMODE.

El esquema PrintTicket aborda cada uno de los dos problemas que se acaban de mencionar. En primer lugar, el esquema PrintTicket es un archivo de texto basado en XML, por lo que se eliminan los problemas con la extensibilidad y el control de versiones. En segundo lugar, la información de configuración está disponible para todos los clientes, lo que significa que cualquier cliente o proveedor puede almacenar y recuperar cualquier información contenida en un PrintTicket. Las opciones se describen mediante la misma técnica que utiliza el marco de esquema de impresión y el documento de PrintCapabilities derivado. Por esta razón, el PrintTicket proporciona todas las ventajas de portabilidad posibles del modelo de definición de la opción que se va a realizar. Consulte [Print Schema Framework](print-schema-framework.md) para obtener más información. El público previsto para esta sección incluye los siguientes grupos:

-   Implementadores de una interfaz de proveedor de PrintTicket/PrintCapabilities

-   Consumidores del PrintTicket

-   Clientes de una interfaz de proveedor de PrintTicket/PrintCapabilities

A los miembros de la primera categoría de la lista anterior se les conoce como proveedores de PrintTicket en el resto de esta sección. Los miembros de las dos últimas categorías se conocen como consumidores de PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relación con el esquema de impresión y el esquema de PrintCapabilities

Los esquemas PrintTicket y PrintCapabilities son partes especializadas del esquema de impresión. Las principales diferencias estructurales entre estos subconjuntos del esquema de impresión es que el esquema PrintTicket contiene instancias de Property y ParameterInit que no están contenidas en el esquema PrintCapabilities, mientras que el esquema PrintCapabilities incluye las instancias de Property y ParameterDef que no están contenidas en el esquema PrintTicket. A excepción de estas diferencias, los esquemas de PrintCapabilities y PrintTicket generalmente se reflejan en el contenido, la característica de uso compartido, la opción, la ScoredProperty y las instancias de valor. Cualquier contenido compartido de este tipo debe mantenerse actualizado. Por ejemplo, si se realiza un cambio en la característica MediaSize en el esquema de PrintCapabilities, se debe realizar el mismo cambio en el esquema PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



