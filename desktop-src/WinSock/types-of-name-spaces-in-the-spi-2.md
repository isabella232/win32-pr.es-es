---
description: Los tres tipos de espacios de nombres de Windows Sockets (Winsock) SPI incluyen espacios de nombres dinámicos, estáticos y persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de espacios de nombres en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697481"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipos de espacios de nombres en el SPI

Hay tres tipos diferentes de espacios de nombres en los que se puede registrar un servicio:

-   Dinámica
-   estática
-   Persistente

Los espacios de nombres dinámicos permiten que los servicios se registren en el espacio de nombres sobre la marcha y para que los clientes detecten los servicios disponibles en tiempo de ejecución. Los espacios de nombres dinámicos suelen basarse en difusiones para indicar la disponibilidad continua de un servicio de red. Algunos ejemplos de espacios de nombres dinámicos incluyen el espacio de nombres de SAP que se usa en un entorno de NetWare y el espacio de nombres NBP que usa AppleTalk.

Los espacios de nombres estáticos requieren que todos los servicios se registren con anterioridad, es decir, cuando se crea el espacio de nombres. El DNS es un ejemplo de un espacio de nombres estático. Aunque hay una manera de resolver nombres mediante programación, no hay ninguna manera de registrar los nombres mediante programación.

Los espacios de nombres persistentes permiten que los servicios se registren con el espacio de nombres sobre la marcha. Sin embargo, a diferencia de los espacios de nombres dinámicos, los espacios de nombres persistentes conservan la información de registro en un almacenamiento no volátil donde permanece hasta el momento en que el servicio solicita que se quite. Los espacios de nombres persistentes son typified por servicios de directorio como X. 500 y NDS (servicio de directorio NetWare). Estos entornos permiten agregar, eliminar y modificar las propiedades del servicio. Además, el objeto de servicio que representa el servicio dentro del servicio de directorio podría tener una variedad de atributos asociados al servicio. El atributo más importante para las aplicaciones cliente es la información de direccionamiento del servicio.

 

 



