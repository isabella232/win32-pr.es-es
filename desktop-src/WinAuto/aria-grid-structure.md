---
title: Error de estructura de cuadrícula ARIA
description: Error de estructura de cuadrícula ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797097"
---
# <a name="aria-grid-structure-error"></a>Error de estructura de cuadrícula ARIA

## <a name="text"></a>Texto

El elemento con el rol de **cuadrícula** no tiene una estructura de cuadrícula correspondiente o un marcado accesible.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos personalizados que tienen el atributo **role** establecido en "Grid". No se aplica a las etiquetas de tabla HTML que tienen un **rol** implícito de "Grid".

Un elemento que tiene el atributo **role** establecido en "Grid" debe tener la estructura definida por el rol de cuadrícula de aplicaciones de Internet enriquecidas (WAI-ARIA) accesible desde la iniciativa Web Accessibility, incluido el nombre accesible para la cuadrícula y sus subelementos de encabezado.

Para corregir este error, revise la implementación para asegurarse de que cumple con la especificación WAI-ARIA. En concreto, asegúrese de que la estructura cumple las siguientes reglas.

-   **Grid** contiene elementos **Row** o **filas** .
-   **filas** contiene elementos **Row** .
-   los elementos **Row** contienen elementos **ColumnHeader** o **gridcell** o **rowheader** .

Se debe definir un nombre accesible para los elementos **Grid**, **ColumnHeader**, **gridcell** y **rowheader** mediante uno de los siguientes atributos.

-   el atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para hacer referencia al elemento que contiene el texto.
-   [**Aria:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) atributo de etiqueta para establecer el nombre accesible directamente.
-   [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) para crear una información sobre herramientas que se usa al mismo tiempo que el nombre.

 

 




