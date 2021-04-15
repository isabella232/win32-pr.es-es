---
title: Serialización de búfer dinámico
description: Cuando se usa el estilo de búfer dinámico de serialización, el código auxiliar asigna el búfer de serialización, y los datos se codifican en este búfer y se devuelven al usuario. Al calcular las referencias, se proporciona el búfer que contiene los datos.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486791"
---
# <a name="dynamic-buffer-serialization"></a>Serialización de búfer dinámico

Cuando se usa el estilo de búfer dinámico de serialización, el código auxiliar asigna el búfer de serialización, y los datos se codifican en este búfer y se devuelven al usuario. Al calcular las referencias, se proporciona el búfer que contiene los datos.

El estilo de búfer dinámico de serialización utiliza las siguientes rutinas:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La función [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) asigna la memoria necesaria para el controlador de codificación y, a continuación, la inicializa. La aplicación puede llamar a [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar el identificador. Llama a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del controlador. Para crear un identificador de descodificación que se corresponda con el controlador de codificación dinámica de búfer, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




