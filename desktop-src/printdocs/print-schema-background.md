---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Fondo del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820442"
---
# <a name="print-schema-background"></a>Fondo del esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión está diseñado para solucionar los problemas de la ambigüedad y la ambigüedad asociada a la comunicación interna entre los componentes del subsistema de impresión y la comunicación externa entre el subsistema de impresión y las aplicaciones.

La interacción actual del subsistema de impresión con los complementos de las aplicaciones y los proveedores de hardware utiliza la estructura de DEVMODE binaria basada en índice y DevCaps binaria. La configuración realizada por cada componente es principalmente opaca para otros componentes, lo que impide la portabilidad de la configuración entre dispositivos o incluso entre diferentes versiones de controladores en el mismo dispositivo. Además, las aplicaciones cliente no pueden aprovechar con facilidad PrintCapabilities sin el conocimiento propietario del dispositivo ni mediante la interfaz de usuario del controlador. Además de estas limitaciones, en un sentido más amplio no hay ningún lenguaje bien definido para describir los atributos generales de los dispositivos, la PrintCapabilities, las configuraciones de dispositivos o el formato de los trabajos. El esquema de impresión y sus tecnologías relacionadas están diseñados para abordar estas limitaciones, lo que proporciona un método coherente, inequívoco y extensible de comunicación de la configuración y las capacidades de una manera consolidada y lógica.

Las bases conceptuales de las palabras clave del esquema de impresión y el marco de trabajo del esquema de impresión son la coherencia, la falta de ambigüedad y la extensibilidad. La coherencia se logra mediante el uso de las palabras clave del esquema de impresión y del marco de esquema de impresión como los bloques de creación para la comunicación entre los componentes de impresión de la próxima generación. Las aplicaciones, el subsistema de impresión de Microsoft Windows y los complementos y controladores IHV interactúan con este mecanismo común. Estas palabras clave, su estructura y su significado estarán bien definidas por el esquema público. Esto evita la ambigüedad en el significado de una palabra clave determinada y evita palabras clave redundantes o duplicadas. Todos los componentes pueden basarse en el uso de una palabra clave determinada para transmitir un determinado intento y hacer que el destinatario lo entienda bien. La extensibilidad es fundamental para ser la longevidad de las palabras clave del esquema de impresión, lo que garantiza que el esquema público sea una entidad dinámica. La estructura también permite extensiones privadas, que concede a los IHV la flexibilidad de innovar según lo deseado, teniendo en cuenta que la inclusión futura de una palabra clave privada en el esquema público es esencial para conservar la coherencia y evitar la ambigüedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



