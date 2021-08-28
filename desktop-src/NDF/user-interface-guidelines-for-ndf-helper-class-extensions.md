---
title: Directrices de interfaz de usuario para extensiones de clase auxiliar de NDF
description: Al compilar la clase auxiliar, deberá crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0094dbee5410d512cfa85f9c227d4b0217f1c507662addb4735023a2ba5833eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801725"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Directrices de interfaz de usuario para extensiones de clase auxiliar de NDF

Al compilar la clase auxiliar, deberá crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.

## <a name="root-cause-and-repair"></a>Causa principal y reparación

Cuando se produce un incidente, aparecerá un cuadro de diálogo para informar al usuario sobre lo que ha ocurrido. El texto que cree aparecerá en dos áreas independientes.

-   **Causa principal:** breve descripción de la causa del problema. Contiene información para ayudar a un administrador o usuario avanzado a solucionar el problema.
-   **Reparación:** expande la causa principal para proporcionar más detalles sobre los pasos que un usuario puede realizar, sin tener que ser demasiado largo.

Cada causa principal o reparación debe tener un título y una descripción. Todo el texto anterior al primer carácter \\ "n" se usará para el título. Se usará todo el texto que sigue al primer carácter "n" (incluidos los saltos de línea \\ posteriores) para la descripción.

## <a name="title-guidelines"></a>Directrices de título

El título de una causa principal o reparación debe seguir estas instrucciones:

-   Debe tener 128 caracteres o menos. (Se recomiendan 40 caracteres o menos).
-   No debe terminar con un punto.

## <a name="description-guidelines"></a>Directrices de descripción

La descripción de una causa principal o reparación debe seguir estas directrices:

-   Debe tener 512 caracteres o menos.
-   Cada frase debe terminar con un punto.
-   El carácter \\ "n" se puede usar para crear un salto de línea en la descripción.

 

 




