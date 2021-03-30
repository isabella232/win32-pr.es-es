---
description: La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Diseño para disponibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538812"
---
# <a name="designing-for-availability"></a>Diseño para disponibilidad

La disponibilidad es la capacidad de una aplicación para tolerar errores en los recursos del servidor. Esto significa que el cliente sigue atendiendo a través del error y que, idealmente, el error es transparente para el cliente. Obviamente, el error puede proviene de orígenes de hardware o software, por lo que debe desarrollar para ambos casos.

La disponibilidad puede verse afectada por los siguientes factores:

-   Modelo de aplicación. Para obtener la máxima disponibilidad, asegúrese de que la lógica de la aplicación crítica se realiza mediante el servicio de [transacciones de com+](com--transactions.md) . Además, el uso de un mecanismo de compensación puede ser eficaz para garantizar que los recursos permanecen en un estado correcto después de los errores.
-   Modelo de cliente. Integre la lógica de "reintento en caso de error" en la aplicación cliente y procurar una degradación correcta en la aplicación si los recursos o servicios no están disponibles. Comprenda lo que el cliente espera de la aplicación y cree un diseño que permita alternativas cuando se produce un error.
-   Disponibilidad de datos y estado. Para obtener acceso coherente a los datos persistentes, utilice la organización por clústeres de Windows para proporcionar compatibilidad con la conmutación por error.
-   Disponibilidad del servicio. Puede usar el equilibrio de carga de red para equilibrar la carga de las solicitudes IP entrantes a través de un clúster de servidores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar para la implementación](designing-for-deployment.md)
</dt> <dt>

[Diseño para la escalabilidad](designing-for-scalability.md)
</dt> <dt>

[Diseñar para la seguridad](designing-for-security.md)
</dt> </dl>

 

 



