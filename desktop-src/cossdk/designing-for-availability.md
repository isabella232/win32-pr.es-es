---
description: La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Diseño para disponibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f248b9ac9ed91788713e7ef02b4e7da0a2d7eb0c2070b1240e07dbce21b5895c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637665"
---
# <a name="designing-for-availability"></a>Diseño para disponibilidad

La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor. Esto significa que el cliente se sigue ateniendo a través del error y que, idealmente, el error es transparente para el cliente. Obviamente, el error puede deber a orígenes de hardware o software, por lo que debe desarrollar en ambos casos.

La disponibilidad puede verse afectada por los siguientes factores:

-   Modelo de aplicación. Para obtener la máxima disponibilidad, asegúrese de que la lógica de aplicación crítica se lleva a cabo mediante el [servicio de transacciones COM+.](com--transactions.md) Además, el uso de un mecanismo de compensación puede ser eficaz para garantizar que los recursos permanezcan en un estado correcto después de los errores.
-   Modelo de cliente. Integre la lógica de "reintento en caso de error" en la aplicación cliente y procure una degradación correcta en la aplicación si los recursos o servicios no están disponibles. Comprenda lo que el cliente espera de la aplicación y cree un diseño que permita alternativas cuando se produzca un error.
-   Disponibilidad de datos/estado. Para un acceso coherente a los datos persistentes, use Windows clustering para proporcionar compatibilidad con la conmutación por error.
-   Disponibilidad del servicio. Puede usar equilibrio de carga de red para equilibrar la carga de las solicitudes IP entrantes en un clúster de servidores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Diseño para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



