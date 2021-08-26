---
description: Tablet PC incluye tecnología para reconocer la entrada de lápiz que se encuentra normalmente en forma de escritura a mano.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Acerca del reconocimiento de escritura a mano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4106d887eaa5bae2a162ab3c08a42c0d3b425b05a09b50bfcde626c05707f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884055"
---
# <a name="about-handwriting-recognition"></a>Acerca del reconocimiento de escritura a mano

Tablet PC incluye tecnología para reconocer la entrada de lápiz que se encuentra normalmente en forma de escritura a mano. El módulo de software que proporciona el reconocimiento se denomina reconocedor. Un reconocedor reconoce un idioma, un grupo de idiomas relacionados o una clase de objetos relacionados, como notas musicales, gestos del sistema o formas geométricas. Puede agregar reconocedores dinámicamente al sistema de servicios ink.

## <a name="recognition-steps"></a>Pasos de reconocimiento

El reconocimiento se controla mediante el uso de un contexto de reconocedor. El reconocimiento consta de cuatro pasos básicos:

1.  Para configurar las restricciones de reconocimiento, haga lo siguiente:
    -   Seleccionar el reconocedor y el modo de entrada (restricciones geométricas).
    -   Establecer las restricciones de lenguaje. Por ejemplo, puede restringir la entrada a caracteres alfanuméricos o puede pasar esquemas para ayudar al reconocedor.
2.  Envío de lápiz al reconocedor.
3.  Procesamiento de la entrada (reconocimiento).
4.  Devolver los resultados del reconocimiento.

Los pasos 2 y 3 se pueden repetir en un bucle o todos los trazos de lápiz se pueden agregar a la entrada de lápiz antes de intentar el reconocimiento.

## <a name="samples-and-related-topics"></a>Ejemplos y temas relacionados

[Ejemplo de reconocimiento avanzado](advanced-recognition-sample.md) muestra cómo usar reconocedores con objetos [**ink**](inkdisp-class.md) para realizar el reconocimiento de lápiz.

[La plantilla de ejemplo de DLL de reconocedor](recognizer-dll-sample-template.md) contiene una plantilla para crear un archivo DLL de reconocedor. La plantilla contiene funciones para registrar y anular el registro del servidor, así como esqueletos para las funciones de reconocedor principal.

En las secciones siguientes se describen los conceptos básicos detrás de la tecnología de reconocimiento de Tablet PC. Para obtener información detallada sobre cómo crear reconocedores personalizados, vea [Creación de un reconocedor.](creating-a-recognizer.md)

-   [Reconocedores de texto](text-recognizers.md)
-   [Reconocedores de objetos](object-recognizers.md)
-   [Uso de la colección Recognizers](using-the-recognizers-collection.md)
-   [Contexto del reconocedor](recognizer-context.md)
-   [Segmentos de reconocimiento](recognition-segments.md)
-   [Reconocimiento de texto angular](recognition-of-angled-text.md)
-   [Compatibilidad con la reordenación de trazos del reconocedor](recognizer-stroke-reordering-support.md)
-   [Diccionarios y factoids](dictionaries-and-factoids.md)
-   [Propiedad de confianza \[ sobre el reconocimiento\]](confidence-property--about-recognition.md)
-   [Alternativas](alternates.md)
-   [Segmentos de entrada de lápiz y alternativas](ink-segments-and-alternates.md)

 

 



