---
description: Los tres tipos de espacios de nombres del SPI Windows Sockets (Winsock) incluyen espacios de nombres dinámicos, estáticos y persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de espacios de nombres en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec933650825e891a723cbbc041ad4f631c6f54b7b2b4f6a255359b640509ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733195"
---
# <a name="types-of-namespaces-in-the-spi"></a>Tipos de espacios de nombres en el SPI

Hay tres tipos diferentes de espacios de nombres en los que se podría registrar un servicio:

-   Dinámica
-   estática
-   Persistente

Los espacios de nombres dinámicos permiten que los servicios se registren con el espacio de nombres sobre la marcha y que los clientes detecte los servicios disponibles en tiempo de ejecución. Los espacios de nombres dinámicos suelen basarse en difusión para indicar la disponibilidad continua de un servicio de red. Algunos ejemplos de espacios de nombres dinámicos son el espacio de nombres de SAP que se usa en un entorno de NetWare y el espacio de nombres NBP que usa AppleTalk.

Los espacios de nombres estáticos requieren que todos los servicios se registren con antelación, es decir, cuando se crea el espacio de nombres. El DNS es un ejemplo de un espacio de nombres estático. Aunque hay una manera de resolver nombres mediante programación, no hay ninguna manera de registrar nombres mediante programación.

Los espacios de nombres persistentes permiten que los servicios se registren con el espacio de nombres sobre la marcha. Sin embargo, a diferencia de los espacios de nombres dinámicos, los espacios de nombres persistentes conservan la información de registro en el almacenamiento no volátil donde permanece hasta el momento en que el servicio solicita que se quite. Los espacios de nombres persistentes se tipifica por servicios de directorio como X.500 y NDS (NetWare Directory Service). Estos entornos permiten agregar, eliminar y modificar las propiedades del servicio. Además, el objeto de servicio que representa el servicio dentro del servicio de directorio podría tener una variedad de atributos asociados al servicio. El atributo más importante para las aplicaciones cliente es la información de direccionamiento del servicio.

 

 



