---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418549"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Texto

La tabulación ha pasado a un elemento fuera del HWND de destino.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El uso de la navegación con el teclado estándar (TAB o Mayús + Tab) hace que el foco se desplace fuera del HWND del destino de la comprobación.

AccChecker sube el árbol de elementos hasta el HWND de nivel superior para el destino de comprobación elegido antes de ejecutar cualquier tarea de comprobación. Esto reduce el número de errores falsos generados si un HWND elegido para la comprobación forma parte de un área cliente más compleja.

## <a name="possible-causes"></a>Causas posibles

-   El destino de la comprobación no requiere una implementación de tabulación para proporcionar toda la funcionalidad.
-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.

 

 




