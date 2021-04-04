---
title: Identificadores de serialización
description: Una aplicación utiliza los procedimientos de serialización o las rutinas de compatibilidad de serialización generadas por el compilador de MIDL junto con un conjunto de funciones de biblioteca para manipular un identificador de serialización.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076168"
---
# <a name="serialization-handles"></a>Identificadores de serialización

Una aplicación utiliza los procedimientos de serialización o las rutinas de compatibilidad de serialización generadas por el compilador de MIDL junto con un conjunto de funciones de biblioteca para manipular un identificador de serialización. Juntas, estas funciones proporcionan un mecanismo para personalizar la manera en que una aplicación serializa los datos.

Se requiere un identificador de serialización para cualquier operación de serialización y todos los identificadores de serialización deben administrarse explícitamente por el usuario. Para ello, primero debe crear un identificador válido mediante una llamada a una de las siguientes rutinas:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Libera el identificador con una llamada a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree). Una vez que se ha creado o reinicializado el identificador, representa un contexto de serialización válido y se puede usar para codificar o descodificar, dependiendo del tipo de identificador.

En esta sección se describen los identificadores de serialización y cómo usarlos en los temas siguientes:

-   [Identificadores implícitos e explícitos](implicit-versus-explicit-handles.md)
-   [Estilos de serialización](serialization-styles.md)
-   [Obtener una identidad de codificación](obtaining-an-encoding-identity.md)

 

 




