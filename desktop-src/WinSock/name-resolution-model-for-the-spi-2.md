---
description: Modelo de registro y resolución de nombres para el SPI de Windows Sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modelo de resolución de nombres para SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154262"
---
# <a name="name-resolution-model-for-the-spi"></a>Modelo de resolución de nombres para SPI

En el desarrollo de una aplicación cliente/servidor independiente del Protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:

-   La capacidad de la mitad del servidor de la aplicación (a la que se hace referencia como servicio) para registrar su existencia en uno o varios espacios de nombres (o ser accesibles).
-   La capacidad de la aplicación cliente de buscar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte y la información de direccionamiento necesarios.

Para aquellos que están acostumbrados a desarrollar aplicaciones basadas en TCP/IP, esto puede suponer un poco más que buscar una dirección de host y, a continuación, usar un número de Puerto acordado. Otros esquemas de red, sin embargo, permiten la ubicación del servicio, el protocolo usado para el servicio y otros atributos que se detectan en tiempo de ejecución. Para acomodar el intervalo de capacidades que se encuentran en los servicios de nombres existentes, la interfaz de Windows Sockets 2 adopta el modelo que se describe a continuación.

Un *espacio de nombres* hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y el direccionamiento de los atributos de un servicio de red con uno o más nombres descriptivos. Muchos espacios de nombres están actualmente en uso amplio, incluidos el sistema de nombres de dominio (DNS) de Internet, Servicios de directorio NetWare (NDS), X. 500, etc. Estos espacios de nombres varían considerablemente en el modo en que se organizan e implementan. Algunas de sus propiedades son especialmente importantes para comprender desde la perspectiva de la resolución de nombres de Windows Sockets.

 

 



