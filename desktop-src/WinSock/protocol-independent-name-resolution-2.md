---
description: Resolución de nombres independiente del protocolo y Windows sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Protocol-Independent resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f214619d4bf54f3ac39d24008f07aa12715fc75ac1bf6ea74280ed80d31d7bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993605"
---
# <a name="protocol-independent-name-resolution"></a>Protocol-Independent resolución de nombres

Al desarrollar una aplicación cliente/servidor independiente del protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:

-   La capacidad de la mitad del servidor de la aplicación (servicio) de registrar su existencia dentro de uno o más espacios de nombres (o ser accesibles para ellos).
-   La capacidad de la aplicación cliente de encontrar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte necesario y la información de direccionamiento.

Para aquellos que están acostumbrados a desarrollar aplicaciones basadas en TCP/IP, puede parecer que esto puede implicar poco más que buscar una dirección de host y, a continuación, usar un número de puerto acordado. Sin embargo, otros esquemas de red permiten detectar la ubicación del servicio, el protocolo usado para el servicio y otros atributos en tiempo de ejecución. Para dar cabida a la amplia diversidad de funcionalidades que se encuentran en los servicios de nombres existentes, la interfaz Windows Sockets 2 adopta el modelo descrito en los temas de esta sección.

En esta sección se describen las funcionalidades de resolución de nombres independientes del protocolo disponibles para los desarrolladores de Winsock. En la lista siguiente se describen los temas de esta sección:

-   [Modelo de resolución de nombres](name-resolution-model-2.md)
-   [Resumen de las funciones de resolución de nombres](summary-of-name-resolution-functions-2.md)
-   [Estructuras de datos de resolución de nombres](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



