---
title: Información general sobre las tablas de descriptores
description: 'Cada tabla de descriptores almacena descriptores de uno o varios tipos: SRV, UAVe, CBV y Samplers. Una tabla descriptora no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da614063f5584369009367c03d0b087b808a60eb0979f1bfad07af128280ee25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098110"
---
# <a name="descriptor-tables-overview"></a>Información general sobre las tablas de descriptores

Cada tabla de descriptores almacena descriptores de uno o varios tipos &mdash; DEV, UAVe, CBV y muestreadores. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.

## <a name="referencing-descriptor-tables"></a>Hacer referencia a tablas descriptores

La canalización de gráficos, a través de la firma raíz, obtiene acceso a los recursos haciendo referencia a tablas descriptores por índice.

Una tabla de descriptores es en realidad solo un sub intervalo de un montón de descriptores. Los montones de descriptores representan la asignación de memoria subyacente para una colección de descriptores. Puesto que la asignación de memoria es una propiedad de un montón de descriptores, se garantiza que definir una tabla de descriptores fuera de uno es tan barato como identificar una región del montón para el hardware. Las tablas de descriptores no tienen que crearse ni destruirse en el nivel de API; simplemente se identifican para los controladores como un desplazamiento y un tamaño fuera de un montón siempre que se hace referencia a ellas.

Sin duda, es posible que una aplicación defina tablas de descriptores muy grandes cuando sus sombreadores desean la libertad de seleccionar de un amplio conjunto de descriptores disponibles (a menudo haciendo referencia a texturas) sobre la marcha (quizás controlados por datos de material).

La firma raíz hace referencia a la entrada de tabla descriptor con una referencia al montón, la ubicación inicial de la tabla (un desplazamiento desde el principio del montón) y la longitud (en entradas) de la tabla. En la imagen siguiente se muestran estos conceptos: los punteros de tabla descriptor de la firma raíz y los descriptores del montón de descriptores que hacen referencia a la textura completa o a los datos del búfer en un montón (en el caso de una textura, el montón predeterminado).

![tablas descriptores](images/descriptor-table.png)

## <a name="related-topics"></a>Temas relacionados

* [Tablas de descriptores](descriptor-tables.md)
