---
title: Identificadores de serialización
description: Una aplicación usa los procedimientos de serialización o las rutinas de compatibilidad de serialización generadas por el compilador midl junto con un conjunto de funciones de biblioteca para manipular un identificador de serialización.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473541"
---
# <a name="serialization-handles"></a>Identificadores de serialización

Una aplicación usa los procedimientos de serialización o las rutinas de compatibilidad de serialización generadas por el compilador midl junto con un conjunto de funciones de biblioteca para manipular un identificador de serialización. Juntas, estas funciones proporcionan un mecanismo para personalizar la forma en que una aplicación serializa los datos.

Se requiere un identificador de serialización para cualquier operación de serialización y el usuario debe administrar explícitamente todos los identificadores de serialización. Para ello, primero debe crear un identificador válido llamando a una de las rutinas siguientes:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

El identificador se libera con una llamada a [**MesHandleFree.**](/windows/desktop/api/Midles/nf-midles-meshandlefree) Una vez creado o reinicializado el identificador, representa un contexto de serialización válido y se puede usar para codificar o descodificar, dependiendo del tipo del identificador.

En esta sección se describen los identificadores de serialización y cómo usarlos en los temas siguientes:

-   [Identificadores implícitos frente a explícitos](implicit-versus-explicit-handles.md)
-   [Estilos de serialización](serialization-styles.md)
-   [Obtener una identidad de codificación](obtaining-an-encoding-identity.md)

 

 




