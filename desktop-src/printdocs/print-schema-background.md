---
description: El esquema de impresión aborda la opacidad y ambigüedad en la comunicación entre los componentes del subsistema de impresión y entre el subsistema de impresión y las aplicaciones.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Fondo del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab366429623f2bb1f187294705d1a83e93acd1e5fb500d4b1e9d224496ac39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731765"
---
# <a name="print-schema-background"></a>Fondo del esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión está pensado para solucionar los problemas de opacidad y ambigüedad asociados a la comunicación interna entre los componentes del subsistema de impresión y la comunicación externa entre el subsistema de impresión y las aplicaciones.

La interacción actual del subsistema de impresión con los complementos de los proveedores de hardware y aplicaciones usa la estructura DEVMODE binaria basada en índices y devCaps binaria. Configuración que realiza cada componente son en gran medida opacos para otros componentes, lo que impide la portabilidad de la configuración entre dispositivos o incluso entre diferentes versiones de controlador en el mismo dispositivo. Además, las aplicaciones cliente no pueden aprovechar fácilmente PrintCapabilities sin conocimientos propietarios del dispositivo o mediante la interfaz de usuario (UI) del controlador. Además de estas limitaciones, en un sentido más amplio no hay ningún lenguaje bien definido para describir atributos generales de dispositivo, PrintCapabilities, configuraciones de dispositivo o formato de trabajo. El esquema de impresión y sus tecnologías relacionadas están diseñados para abordar estas limitaciones, proporcionando un método coherente, inequívoque y extensible de comunicación de configuración y funcionalidades de una manera consolidada y lógica.

Los fundamentos conceptuales de las palabras clave de esquema de impresión y el marco de esquema de impresión son la coherencia, la falta de ambigüedad y la extensibilidad. La coherencia se logra mediante el uso de las palabras clave de esquema de impresión y el marco de esquema de impresión como bloques de creación para la comunicación entre los componentes de impresión de próxima generación. Las aplicaciones, el subsistema Windows de impresión de Microsoft y los complementos y controladores de IHV interactúan mediante este mecanismo común. Estas palabras clave, su estructura y su significado estarán bien definidas por el esquema público. Esto evita la ambigüedad en el significado de una palabra clave determinada y evita palabras clave redundantes o duplicadas. Todos los componentes pueden basarse en el uso de una palabra clave determinada para transmitir una determinada intención y que el destinatario la entienda bien. La extensibilidad es fundamental para ser la longevidad de las palabras clave de esquema de impresión, lo que garantiza que el esquema público es una entidad dinámica. La estructura también permite extensiones privadas, que conceden a los IHV la flexibilidad necesaria para innovar, teniendo en cuenta que la inclusión futura de una palabra clave privada en el esquema público es esencial para conservar la coherencia y evitar la ambigüedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



