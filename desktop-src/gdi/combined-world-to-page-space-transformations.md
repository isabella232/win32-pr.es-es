---
description: Las cinco transformaciones de mundo a página se pueden combinar en una única matriz 3 por 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformaciones combinadas de espacio de mundo a página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70be3bca8687b89bbb2a50fefaaae70fea9b5f86c1762c4414a3974793ea8d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887505"
---
# <a name="combined-world-to-page-space-transformations"></a>Transformaciones combinadas de espacio de mundo a página

Las cinco transformaciones de mundo a página se pueden combinar en una única matriz 3 por 3. La [**función CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) se puede usar para combinar dos transformaciones de espacio del mundo a espacio de página. Las transformaciones combinadas se pueden usar para modificar la salida asociada a un contexto de dispositivo (DC) determinado llamando a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) y suministrando los elementos para esta matriz. Cuando una aplicación llama **a SetWorldTransform**, almacena los elementos de la matriz 3 por 3 en una [**estructura XFORM.**](/windows/win32/api/wingdi/ns-wingdi-xform) Los miembros de esta estructura corresponden a las dos primeras columnas de una matriz 3 por 3; La última columna de la matriz no es necesaria porque sus valores son constantes.

Los elementos de la matriz de transformación del mundo actual se pueden reactivar llamando a la función [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) y suministrando un puntero a una [**estructura XFORM.**](/windows/win32/api/wingdi/ns-wingdi-xform)

 

 



