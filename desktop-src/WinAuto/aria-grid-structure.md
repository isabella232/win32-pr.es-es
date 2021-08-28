---
title: Error de estructura de cuadrícula de ARIA
description: Error de estructura de cuadrícula de ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b91010417ed01f211859839ceab124b299b10679b3d460f860c03e5b2473f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122385"
---
# <a name="aria-grid-structure-error"></a>Error de estructura de cuadrícula de ARIA

## <a name="text"></a>Texto

El elemento con **el rol de** cuadrícula no tiene una estructura de cuadrícula correspondiente o marcado accesible.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos personalizados que tienen el **atributo role** establecido en "grid". No se aplica a las etiquetas de tabla HTML que tienen un **rol implícito** de "grid".

Un elemento que  tenga su atributo de rol establecido en "grid" debe tener la estructura definida por el rol de cuadrícula Iniciativa de accesibilidad web- Aplicaciones de Internet enriqueidas accesibles (IAM-ARIA), incluido el nombre accesible para la cuadrícula y sus subelementos de encabezado.

Para corregir este error, revise la implementación para asegurarse de que cumple con la especificación DEIA-ARIA. En concreto, asegúrese de que la estructura cumple las siguientes reglas.

-   **grid** contiene **elementos row** o **rowgroup.**
-   **el grupo de filas** contiene **elementos de** fila.
-   **Los elementos row** contienen **elementos columnheader,** **gridcell** o **rowheader.**

Se debe definir un nombre accesible para los elementos **grid**, **columnheader,** **gridcell** y **rowheader** mediante uno de los atributos siguientes.

-   [**Atributo aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para hacer referencia al elemento que contiene texto.
-   [**Atributo aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para establecer el nombre accesible directamente.
-   [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) para crear una información sobre herramientas que se usa al mismo tiempo como nombre.

 

 




