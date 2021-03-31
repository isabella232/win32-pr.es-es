---
title: La funcionalidad de la aplicación de escritorio se ve afectada si no se ejecuta en modo de ventana
description: En Windows 10, las aplicaciones de Windows ya no se muestran en pantalla completa de forma predeterminada; en su lugar, se encuentran en ventanas y las operaciones como la minimización, la restauración, la maximización, el cambio de tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana clásica de la aplicación Windows) ahora son posibles.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418984"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>La funcionalidad de la aplicación de escritorio se ve afectada si no se ejecuta en modo de ventana

En Windows 10, las aplicaciones de Windows ya no se muestran en pantalla completa de forma predeterminada; en su lugar, se encuentran en ventanas y las operaciones como la minimización, la restauración, la maximización, el cambio de tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana clásica de la aplicación Windows) ahora son posibles.

## <a name="manifestations"></a>Manifestaciones

El cambio más notable ahora es que puede obtener el tamaño de los tamaños arbitrarios que no son solo el tamaño de la pantalla o el alto de la pantalla. Un usuario puede cambiar continuamente el tamaño de la ventana de la aplicación a su gusto (hasta el tamaño mínimo de la ventana de la aplicación). Esto es diferente de Windows 8,0 o Windows 8.1, donde el acto de cambiar el tamaño de una ventana era una acción discreta (los usuarios cambiaron el tamaño de una vista en miniatura de la ventana, lo que hacía que la ventana cambiara de tamaño una vez que el usuario confirmó la acción). En la actualidad, cuando el usuario arrastra la ventana por la esquina inferior (u otra ubicación del borde), es un cambio de tamaño continuo y la aplicación recibe los mensajes de cambio de tamaño en una fila, en lugar de cambiar el tamaño.

## <a name="mitigations"></a>Mitigaciones

Para mitigar este riesgo en aplicaciones Windows 8,0 y 8,1:

-   Si se interrumpe la característica esperada dentro de la funcionalidad de la aplicación, la mitigación del usuario es poner la aplicación en modo de pantalla completa (con el botón "ir a pantalla completa" en la esquina superior derecha de la barra de título).
-   Si el inicio de la aplicación se ve afectado porque no se abre según lo esperado, el usuario todavía debe poder cambiar al modo de Tablet PC para forzar que la aplicación se inicie en modo de pantalla completa sin la intervención del usuario.

La mejor manera de controlarlo es cambiar la aplicación para que tenga en cuenta el hecho de que puede ajustarse a las posiciones y los altos de tamaño sin supervisión (es decir, no tener una tabla codificada de alto y ancho y esperar también las proporciones codificadas de forma rígida). Los desarrolladores de aplicaciones deberían esperar que se cambie el tamaño de la aplicación, otro mensaje de cambio de tamaño puede producirse justo después de que se entregue el mensaje de cambio de tamaño actual: como resultado, si la aplicación inicia animaciones durante el cambio de tamaño, es posible que la aplicación reciba otro mensaje de cambio de tamaño justo después (por lo que es importante asegurarse de que este tipo de situación no conduce al bloqueo de la aplicación).

 

 




