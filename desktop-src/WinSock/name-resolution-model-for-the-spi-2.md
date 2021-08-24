---
description: Resolución de nombres y modelo de registro para Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modelo de resolución de nombres para spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f012a5c14a6dae9045b303ecb7c4e39f1d93d264285138d98c0e93274ef921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132118"
---
# <a name="name-resolution-model-for-the-spi"></a>Modelo de resolución de nombres para spi

Al desarrollar una aplicación cliente/servidor independiente del protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:

-   La capacidad de la mitad del servidor de la aplicación (que en adelante se conoce como servicio) para registrar su existencia dentro de uno o varios espacios de nombres( o ser accesibles para ellos).
-   La capacidad de la aplicación cliente de encontrar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte necesario y la información de direccionamiento.

Para aquellos acostumbrados a desarrollar aplicaciones basadas en TCP/IP, esto puede implicar poco más que buscar una dirección de host y, a continuación, usar un número de puerto acordado. Sin embargo, otros esquemas de red permiten detectar la ubicación del servicio, el protocolo usado para el servicio y otros atributos en tiempo de ejecución. Para dar cabida al intervalo de funcionalidades que se encuentran en los servicios de nombres existentes, la interfaz Windows Sockets 2 adopta el modelo que se describe a continuación.

Un *espacio* de nombres hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y los atributos de direccionamiento de un servicio de red con uno o varios nombres descriptivos para el usuario. Muchos espacios de nombres están actualmente en uso general, incluidos el Sistema de nombres de dominio (DNS) de Internet, Servicios de directorio NetWare (NDS), X.500, etc. Estos espacios de nombres varían ampliamente en la forma en que se organizan e implementan. Algunas de sus propiedades son especialmente importantes para comprender desde la perspectiva de la Windows nombres de sockets.

 

 



