---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077975"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Texto

El tabulador de esta aplicación no es cíclico. Los tiempos de tabulación hacia delante o hacia atrás {0} no vuelven al mismo control.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Cuando se usa la navegación de teclado estándar (TAB o Mayús + Tab), no es posible atravesar el árbol de elementos del destino de comprobación hasta que el elemento inicial se convierta en el elemento final (con el mismo número de pulsaciones de teclas) invirtiendo la dirección del recorrido. Por ejemplo, la tabulación hacia delante (tabulación) x veces desde el elemento a (0) hasta el elemento A (x) y, a continuación, la tabulación hacia atrás (Mayús + Tab) x veces no da lugar a que el elemento A (0) vuelva a obtener el foco.

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque no hay ninguna manera predecible de volver a un control una vez que se ha visitado.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario es un control personalizado que no implementa el tabulador correctamente. Por ejemplo, la propiedad estado de MSAA no se ha establecido correctamente.
-   Algunas aplicaciones, como el Bloc de notas, muestran este comportamiento de forma inconsistente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el diseño de la interfaz de usuario de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 