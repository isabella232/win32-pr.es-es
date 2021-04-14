---
description: Resolución de nombres independiente del protocolo y Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Resolución de nombres de Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360294"
---
# <a name="protocol-independent-name-resolution"></a>Resolución de nombres de Protocol-Independent

En el desarrollo de una aplicación cliente/servidor independiente del Protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:

-   La capacidad de la mitad del servidor de la aplicación (servicio) de registrar su existencia en uno o varios espacios de nombres (o se puede tener acceso a ellos).
-   La capacidad de la aplicación cliente de buscar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte y la información de direccionamiento necesarios.

En el caso de los usuarios acostumbrados a desarrollar aplicaciones basadas en TCP/IP, esto puede parecer un poco más que buscar una dirección de host y, a continuación, usar un número de Puerto acordado. Sin embargo, otros esquemas de red permiten la ubicación del servicio, el protocolo usado para el servicio y otros atributos que se detectan en tiempo de ejecución. Para dar cabida a la amplia diversidad de capacidades que se encuentran en los servicios de nombres existentes, la interfaz de Windows Sockets 2 adopta el modelo descrito en los temas de esta sección.

En esta sección se describen las capacidades de resolución de nombres independientes del protocolo disponibles para los desarrolladores de Winsock. En la lista siguiente se describen los temas de esta sección:

-   [Modelo de resolución de nombres](name-resolution-model-2.md)
-   [Resumen de las funciones de resolución de nombres](summary-of-name-resolution-functions-2.md)
-   [Estructuras de datos de resolución de nombres](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



