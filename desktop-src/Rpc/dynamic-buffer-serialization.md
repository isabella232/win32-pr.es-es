---
title: Serialización dinámica de búfer
description: Cuando se usa el estilo de búfer dinámico de serialización, el búfer de serialización se asigna mediante el código auxiliar y los datos se codifican en este búfer y se le pasan de vuelta. Al desmarque, proporcione el búfer que contiene los datos.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea47a87a9d2e566dcfb033b0c9e9403ae72081afe0a1554337dbacfef9c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021685"
---
# <a name="dynamic-buffer-serialization"></a>Serialización dinámica de búfer

Cuando se usa el estilo de búfer dinámico de serialización, el búfer de serialización se asigna mediante el código auxiliar y los datos se codifican en este búfer y se le pasan de vuelta. Al desmarque, proporcione el búfer que contiene los datos.

El estilo de búfer dinámico de serialización usa las rutinas siguientes:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La [**función MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) asigna la memoria necesaria para el identificador de codificación y, a continuación, la inicializa. La aplicación puede llamar [**a MesBufferHandleReset para**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) reinicializar el identificador. Llama a [**MesHandleFree para**](/windows/desktop/api/Midles/nf-midles-meshandlefree) liberar la memoria del identificador. Para crear un identificador de descodificación correspondiente al identificador de codificación de búfer dinámico, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




