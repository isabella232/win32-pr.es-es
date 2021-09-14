---
title: La funcionalidad de la aplicación de escritorio se afecta si no se ejecuta en modo de ventana
description: En Windows 10, las aplicaciones de Windows ya no son de pantalla completa de forma predeterminada; en su lugar, se abren ventanas y ahora es posible realizar operaciones como minimizar, restaurar, maximizar, cambiar el tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana de aplicación clásica de Windows).
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362826"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>La funcionalidad de la aplicación de escritorio se afecta si no se ejecuta en modo de ventana

En Windows 10, las aplicaciones de Windows ya no son de pantalla completa de forma predeterminada; en su lugar, se abren ventanas y ahora es posible realizar operaciones como minimizar, restaurar, maximizar, cambiar el tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana de aplicación clásica de Windows).

## <a name="manifestations"></a>Manifestaciones

El cambio más evidente ahora es que puede cambiar de tamaño a tamaños arbitrarios que no son solo el tamaño de la pantalla o el alto de la pantalla. Un usuario puede cambiar continuamente el tamaño de la ventana de la aplicación a su gusto (hasta el tamaño mínimo de la ventana de la aplicación). Esto es diferente de Windows 8.0 o Windows 8.1, donde el acto de cambiar el tamaño de una ventana era una acción discreta (los usuarios cambiaron el tamaño de una miniatura de la ventana, lo que hizo que la ventana cambiara de tamaño una vez que el usuario confirmaba la acción). En su lugar, cuando el usuario arrastra la ventana por la esquina inferior (u otra ubicación del borde), es un cambio de tamaño continuo y la aplicación recibe mensajes de cambio de tamaño en una fila, en lugar de cambiar el tamaño.

## <a name="mitigations"></a>Mitigaciones

Para mitigar esto para Windows 8.0 y 8.1:

-   Si la característica esperada dentro de la funcionalidad de la aplicación está rota, la mitigación del usuario es colocar la aplicación en modo de pantalla completa (mediante el botón "Ir a pantalla completa" en la esquina superior derecha de la barra de título).
-   Si el inicio de la aplicación se ha afectado porque no se abre según lo previsto, el usuario todavía debería poder cambiar al modo de tableta para forzar que la aplicación se inicie en modo de pantalla completa sin intervención del usuario.

La mejor manera de controlar esto es cambiar la aplicación para que tenga en cuenta el hecho de que se puede ajustar a lugares y alturas sin tamaño de supervisión (es decir, no tiene una tabla codificada de alto/anchos y solo espera esas proporciones codificadas de forma rígida). Los desarrolladores de aplicaciones deben esperar que, a medida que se cambia el tamaño de la aplicación, se pueda producir otro mensaje de cambio de tamaño justo después de entregar el mensaje de cambio de tamaño actual; como resultado, si la aplicación inicia animaciones durante el cambio de tamaño, es posible que la aplicación reciba otro mensaje de cambio de tamaño inmediatamente después (por lo que es importante asegurarse de que este tipo de situación no conduce a que la aplicación se bloquea).

 

 




