---
title: Información general sobre las tablas de descriptores
description: 'Cada tabla de descriptores almacena descriptores de uno o varios tipos: SRV, UAVe, CBV y Samplers. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.'
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3edae00c37a451aa0fb71355a1dea5860de4398f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813106"
---
# <a name="descriptor-tables-overview"></a>Información general sobre las tablas de descriptores

Cada tabla de descriptores almacena descriptores de uno o varios tipos &mdash; SRV, UAVe, CBV y samplers. Una tabla de descriptores no es una asignación de memoria; es simplemente un desplazamiento y una longitud en un montón de descriptores.

## <a name="referencing-descriptor-tables"></a>Hacer referencia a tablas de descriptores

La canalización de gráficos, a través de la firma raíz, obtiene acceso a los recursos haciendo referencia a las tablas de descriptores por índice.

En realidad, una tabla de descriptores es solo un sub intervalo de un montón de descriptores. Los montones de descriptores representan la asignación de memoria subyacente para una colección de descriptores. Puesto que la asignación de memoria es una propiedad de un montón de creación de un descriptor, se garantiza que la definición de una tabla de descriptores fuera de uno es tan económica como identificar una región del montón para el hardware. No es necesario crear ni destruir tablas de descriptores en el nivel de API: simplemente se identifican para los controladores como un desplazamiento y un tamaño fuera de un montón siempre que se hace referencia a ellas.

Es ciertamente posible que una aplicación defina tablas de descriptores muy grandes cuando sus sombreadores quieren tener la libertad de seleccionar de un amplio conjunto de descriptores disponibles (a menudo haciendo referencia a texturas) sobre la marcha (quizás controlados por datos de material).

La firma raíz hace referencia a la entrada de la tabla descriptor con una referencia al montón, la ubicación inicial de la tabla (un desplazamiento desde el inicio del montón) y la longitud (en entradas) de la tabla. En la imagen siguiente se muestran estos conceptos: los punteros de tabla de descriptores de la firma raíz y los descriptores del montón de descriptores que hacen referencia a la textura completa o a los datos del búfer en un montón (en el caso de una textura, el montón predeterminado).

![tablas de descriptores](images/descriptor-table.png)

## <a name="related-topics"></a>Temas relacionados

* [Tablas de descriptores](descriptor-tables.md)
