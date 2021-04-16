---
description: Uniscribe proporciona las API para admitir la tipografía y para admitir la visualización y edición de texto internacional, incluidas las complejas reglas de los scripts de Oriente Medio y asiático.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Usar Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678533"
---
# <a name="using-uniscribe"></a>Usar Uniscribe

Uniscribe proporciona las API para admitir la tipografía y para admitir la visualización y edición de texto internacional, incluidas las complejas reglas de los scripts de Oriente Medio y asiático. Uniscribe proporciona rutinas de bajo nivel para controlar el texto con formato completo y un conjunto simple de API ScriptString para el texto sin formato.

Con Uniscribe, las aplicaciones solo tienen que administrar una memoria auxiliar de códigos de caracteres Unicode. Las aplicaciones de diseño de texto no tienen que mantener ningún otro búfer ni tabla de asignación para realizar el seguimiento del orden de los caracteres. Cada aplicación solo tiene que almacenar y administrar el orden en el que el usuario escribe los caracteres, que es el mismo orden lógico definido por Unicode. La memoria auxiliar nunca cambia como resultado de las operaciones de diseño. Uniscribe mantiene un índice de los clústeres reordenados hasta los límites de caracteres originales pasados por la aplicación.

Los temas siguientes se tratan en esta sección.

**Formas**

-   [Determinar si un script requiere la forma de glifos](determining-if-a-script-requires-glyph-shaping.md)
-   [Usar motores de modelado](using-shaping-engines.md)

**Otro procesamiento**

-   [Almacenamiento en caché](caching.md)
-   [Mostrar texto con Uniscribe](displaying-text-with-uniscribe.md)
-   [Procesamiento de scripts complejos](processing-complex-scripts.md)
-   [Usar la reserva de fuentes](using-font-fallback.md)
-   [Uso de las funciones ScriptString](using-the-scriptstring-functions.md)

**Intercalación**

-   [Mostrar el símbolo de intercalación en cadenas bidireccionales](displaying-the-caret-in-bidirectional-strings.md)
-   [Administrar la ubicación del símbolo de intercalación y la prueba de posicionamiento](managing-caret-placement-and-hit-testing.md)
-   [Trasladar el desplazamiento de la X hasta la posición del símbolo de intercalación](translating-mouse-hit-x-offset-to-caret-position.md)

**Palabras y clústeres de caracteres**

-   [Uso de clústeres de caracteres](using-character-clusters.md)
-   [Usar puntos de interrupción de palabras](using-word-break-points.md)
-   [Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



