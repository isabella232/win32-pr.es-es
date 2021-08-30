---
description: Uniscribe proporciona API para admitir la tipografía y para admitir la presentación y edición de texto internacional, incluidas las reglas complejas de los scripts de Oriente Medio y Asia.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Uso de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d5e4b6e02c2d6440281eafff54e43948edbe0a0259e969f3c564effb38092d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130045"
---
# <a name="using-uniscribe"></a>Uso de Uniscribe

Uniscribe proporciona API para admitir la tipografía y para admitir la presentación y edición de texto internacional, incluidas las reglas complejas de los scripts de Oriente Medio y Asia. Uniscribe proporciona rutinas de bajo nivel para controlar texto con formato completo y un sencillo conjunto de API ScriptString para texto sin formato.

Con Uniscribe, las aplicaciones solo tienen que administrar un almacén de respaldo de códigos de caracteres Unicode. Las aplicaciones de diseño de texto no tienen que mantener ningún otro búfer o tabla de asignación para realizar un seguimiento del orden de los caracteres. Cada aplicación solo tiene que almacenar y administrar el orden en el que el usuario especifica los caracteres, que es el mismo orden lógico definido por Unicode. El almacén de respaldo nunca cambia como resultado de las operaciones de diseño. Uniscribe mantiene un índice de los clústeres reordenados a los límites de caracteres originales pasados por la aplicación.

En esta sección se tratan los temas siguientes.

**Formas**

-   [Determinar si un script requiere forma de glifo](determining-if-a-script-requires-glyph-shaping.md)
-   [Uso de motores de modelado](using-shaping-engines.md)

**Otro procesamiento**

-   [Almacenamiento en caché](caching.md)
-   [Mostrar texto con Uniscribe](displaying-text-with-uniscribe.md)
-   [Procesamiento de scripts complejos](processing-complex-scripts.md)
-   [Uso de la reserva de fuentes](using-font-fallback.md)
-   [Uso de las funciones ScriptString](using-the-scriptstring-functions.md)

**Intercalación**

-   [Mostrar el caret en cadenas bidireccionales](displaying-the-caret-in-bidirectional-strings.md)
-   [Administración de la selección de ubicación del caret y las pruebas de posicionamiento](managing-caret-placement-and-hit-testing.md)
-   [Traducción del desplazamiento X de posicionamiento del mouse a la posición del cursor de cursor](translating-mouse-hit-x-offset-to-caret-position.md)

**Palabras y clústeres de caracteres**

-   [Uso de clústeres de caracteres](using-character-clusters.md)
-   [Usar puntos de interrupción de Word](using-word-break-points.md)
-   [Trabajar con relaciones entre posiciones de cursor de referencia, puntos de justificación y clústeres](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



