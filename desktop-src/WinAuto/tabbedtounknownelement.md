---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052403"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Texto

El tabulador ha pasado a un elemento fuera del hwnd de destino.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El uso de la navegación con teclado estándar (Tab o Mayús+Tab) hace que el foco cambie fuera del HWND del destino de comprobación.

AccChecker sube el árbol de elementos al HWND de nivel superior para el destino de comprobación elegido antes de ejecutar las tareas de comprobación. Esto reduce el número de errores falsos generados si un HWND elegido para la comprobación forma parte de un área de cliente más compleja.

## <a name="possible-causes"></a>Causas posibles

-   El destino de comprobación no requiere una implementación de tabulación para proporcionar funcionalidad completa.
-   La interacción del usuario durante la comprobación, como mover el foco a un HWND no de destino, interfirieron con el proceso de comprobación.

 

 




