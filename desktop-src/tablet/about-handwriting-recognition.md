---
description: Tablet PC incluye tecnología para reconocer la entrada manuscrita que suele tener la forma de escritura a mano.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Acerca del reconocimiento de escritura a mano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717220"
---
# <a name="about-handwriting-recognition"></a>Acerca del reconocimiento de escritura a mano

Tablet PC incluye tecnología para reconocer la entrada manuscrita que suele tener la forma de escritura a mano. El módulo de software que proporciona el reconocimiento se denomina reconocedor. Un reconocedor reconoce un idioma, un grupo de idiomas relacionados o una clase de objetos relacionados, como notas musicales, gestos del sistema o formas geométricas. Puede Agregar reconocedores al sistema de servicios de tinta de forma dinámica.

## <a name="recognition-steps"></a>Pasos de reconocimiento

El reconocimiento se controla mediante el uso de un contexto de reconocedor. El reconocimiento consta de cuatro pasos básicos:

1.  Configurar las restricciones de reconocimiento mediante:
    -   Seleccionar el reconocedor y el modo de entrada (restricciones geométricas).
    -   Establecer las restricciones de idioma. Por ejemplo, puede restringir la entrada a caracteres alfanuméricos o puede pasar esquemas para ayudar al reconocedor.
2.  Enviar entradas manuscritas al reconocedor.
3.  Procesar la entrada (reconociendo).
4.  Devolver los resultados del reconocimiento.

Los pasos 2 y 3 pueden repetirse en un bucle, o bien se pueden agregar todos los trazos de lápiz a la tinta antes de que se intente el reconocimiento.

## <a name="samples-and-related-topics"></a>Ejemplos y temas relacionados

El [ejemplo de reconocimiento avanzado](advanced-recognition-sample.md) muestra cómo utilizar los reconocedores con objetos de [**tinta**](inkdisp-class.md) para realizar el reconocimiento de tinta.

La [plantilla de ejemplo de dll de reconocedor](recognizer-dll-sample-template.md) contiene una plantilla para crear un archivo dll de reconocedor. La plantilla contiene funciones para registrar y anular el registro del servidor, así como esqueletos para las funciones principales del reconocedor.

En las secciones siguientes se describen los conceptos básicos de la tecnología de reconocimiento de Tablet PC. Para obtener información detallada acerca de cómo crear reconocedores personalizados, consulte [crear un reconocedor](creating-a-recognizer.md).

-   [Reconocedores de texto](text-recognizers.md)
-   [Reconocedores de objetos](object-recognizers.md)
-   [Usar la colección Recognizers](using-the-recognizers-collection.md)
-   [Contexto del reconocedor](recognizer-context.md)
-   [Segmentos de reconocimiento](recognition-segments.md)
-   [Reconocimiento de texto angulado](recognition-of-angled-text.md)
-   [Compatibilidad de reordenación de trazos de reconocedor](recognizer-stroke-reordering-support.md)
-   [Diccionarios y Factoids](dictionaries-and-factoids.md)
-   [Propiedad Confidence \[ sobre el reconocimiento\]](confidence-property--about-recognition.md)
-   [Alternativas](alternates.md)
-   [Segmentos de tinta y alternativas](ink-segments-and-alternates.md)

 

 



