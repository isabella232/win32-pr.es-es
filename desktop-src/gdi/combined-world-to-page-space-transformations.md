---
description: Las cinco transformaciones de mundo a página se pueden combinar en una sola matriz de 3 por 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformaciones de espacio de página universal combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985026"
---
# <a name="combined-world-to-page-space-transformations"></a>Transformaciones de espacio de página universal combinadas

Las cinco transformaciones de mundo a página se pueden combinar en una sola matriz de 3 por 3. La función [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) se puede usar para combinar dos transformaciones de espacio mundial en la página. Las transformaciones combinadas se pueden usar para modificar la salida asociada a un contexto de dispositivo determinado (DC) mediante una llamada a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) y proporcionando los elementos para esta matriz. Cuando una aplicación llama a **SetWorldTransform**, almacena los elementos de la matriz de 3 por 3 en una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) . Los miembros de esta estructura se corresponden con las dos primeras columnas de una matriz de 3 por 3; la última columna de la matriz no es necesaria porque sus valores son constantes.

Los elementos de la matriz de transformación universal actual se pueden reactivar llamando a la función [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) y proporcionando un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

 



