---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Tecnologías de Schema-Related de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8618493c2d24e8aebd7609c893d9de5a675bf24f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104157056"
---
# <a name="print-schema-related-technologies"></a>Tecnologías de Schema-Related de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En el .NET Framework 3,0, Windows Vista y versiones posteriores, las tecnologías de PrintCapabilities y PrintTicket amplían las capacidades del esquema de impresión para habilitar una experiencia de impresión más enriquecida.

## <a name="printcapabilities"></a>PrintCapabilities

La tecnología de PrintCapabilities es un método de publicación de la descripción de la configuración que controla el usuario de los atributos y la configuración de cada trabajo. PrintCapabilities se publica en un documento de lenguaje de marcado extensible (XML) denominado documento de PrintCapabilities, que consta de los términos definidos en las palabras clave del esquema de impresión y extensiones privadas. El documento de PrintCapabilities se puede considerar como una "instantánea" de la configuración del dispositivo actual del estado configurable del usuario, así como una descripción de las posibles configuraciones. Los dispositivos (o controladores de dispositivos) generan un documento de PrintCapabilities (la instantánea) de su conjunto actual de opciones configurables cuando lo consultan los clientes, que pueden ser aplicaciones o el subsistema de impresión. En este documento se describe toda la PrintCapabilities configurable disponible actualmente en el dispositivo, como opciones de acabado y opciones de diseño de página. El documento de PrintCapabilities describe explícitamente todos los atributos del dispositivo y la configuración permitida para cada atributo. Mediante el uso del marco de trabajo del esquema de impresión, los atributos del dispositivo se pueden describir y comparar de manera precisa. Mediante el uso de las palabras clave contenidas en el documento imprimir palabras clave del esquema y la estructura definida en el marco de trabajo del esquema de impresión, los dispositivos pueden permitir a los clientes usar de forma más eficaz la PrintCapabilities. Para obtener más información, vea [esquema de PrintCapabilities y construcción de documentos](printcapabilities-schema-and-document-construction.md).

En relación con el subsistema de impresión en Microsoft Windows Server 2003 y versiones anteriores, la tecnología de PrintCapabilities permite a los componentes del subsistema de impresión y cliente ver de forma transparente la información contenida en la PrintCapabilities binaria del sistema Win32 actual. Esto permite al cliente consultar PrintCapabilities, recibir una instantánea XML coherente y bien entendida y utilizarla para construir un PrintTicket para un dispositivo sin invocar la interfaz de usuario del controlador (UI).

## <a name="printticket"></a>PrintTicket

La tecnología PrintTicket es el sucesor de la estructura DEVMODE actual. Es un documento basado en lenguaje de marcado extensible que especifica y conserva información sobre el formato del trabajo y la configuración del trabajo de impresión. Una instancia de PrintTicket asigna una configuración de dispositivo determinada y transmite la intención del usuario. Hay dos tipos de elementos PrintTicket: genéricos elementos PrintTicket, que no se generan para un dispositivo determinado. y elementos PrintTicket específicos del dispositivo, que se construyen para un dispositivo determinado. Los elementos PrintTicket genéricos, que están pensados para ser portátiles entre dispositivos, derivan su contenido seleccionando la configuración de cada uno de los atributos de dispositivo descritos exclusivamente en las palabras clave del esquema de impresión. Los elementos PrintTicket específicos del dispositivo derivan su contenido de un documento de PrintCapabilities, seleccionando la configuración de cada atributo de dispositivo anunciado en este documento. Estos elementos PrintTicket también pueden incluir extensiones privadas, específicas de un modelo de dispositivo o familia de modelos de dispositivos. Para obtener más información, vea [esquema de PrintTicket y construcción de documentos](printticket-schema-and-document-construction.md).

En relación con el subsistema de impresión actual, la tecnología PrintTicket permite que todos los componentes y clientes del subsistema de impresión tengan acceso transparente a la información almacenada actualmente en las partes públicas y privadas de la estructura DEVMODE, utilizando un formato XML bien definido. Este diseño resuelve los problemas actuales encontrados en los escenarios de degradación de controladores o degradación y de desigualdad de controladores en los controladores diseñados para la tecnología de PrintTicket. Actualmente, estos escenarios pueden provocar una pérdida de configuración y, por lo tanto, una experiencia de cliente negativa. El PrintTicket también habilita nuevos escenarios, como la habilitación de un controlador de impresora para exponer la configuración de DEVMODE privada en aplicaciones y complementos personalizados de manera coherente e inequívoca. Esto permite que los componentes de impresión sean más transparentes y controlen de forma más limpia las migraciones de configuración. Las interfaces PrintTicket se expondrán a las aplicaciones a través de métodos en objetos de código administrado que también estarán disponibles para los scripts. En el nuevo marco de trabajo de la aplicación basado en objetos de código administrado en el .NET Framework 3,0, el valor de PrintTicket es la forma estándar de describir la configuración del documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



