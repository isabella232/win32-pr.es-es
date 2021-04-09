---
description: El tamaño de los paquetes multimedia afecta a la capacidad de los protocolos IPX para transferir datos a través de redes y puede resultar difícil tratar con un modo independiente del transporte.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Acerca del tamaño del paquete multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f97e36a81b90b72d4d1148e9461f58ae2147ba
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003425"
---
# <a name="about-media-packet-size"></a>Acerca del tamaño del paquete multimedia

El tamaño de los paquetes multimedia afecta a la capacidad de los protocolos IPX para transferir datos a través de redes y puede resultar difícil tratar con un modo independiente del transporte. IPX no segmenta los paquetes, ni informa de Cuándo se quitan los paquetes debido a infracciones de tamaño. Esto significa que alguna entidad de la estación final debe mantener el conocimiento del tamaño máximo de paquete que se va a usar en una ruta de acceso de red determinada. Tradicionalmente, los datagramas IPX y los servicios orientados a la conexión SPX han dejado esta carga en la aplicación, mientras que SPXII ha usado una gran negociación de paquetes de Internet para administrarla de forma transparente.

Winsock intenta establecer límites de tamaño de paquete racional para sus diversos protocolos IPX, tal y como se describe en la sección siguiente. Las aplicaciones pueden ver y modificar estos límites a través de las opciones Get/Set Socket. Al determinar el tamaño máximo de los paquetes, las tres áreas de preocupación son las siguientes:

-   \# Tamaño de paquete multimedia
-   \# Tamaño de paquete enrutable
-   \# Tamaño de paquete de la estación de finalización

El *tamaño de paquete multimedia* refleja el tamaño de paquete máximo aceptable en cualquier medio que el paquete atraviesa a su destino. El tamaño de los paquetes varía entre los distintos medios, como Ethernet y token ring. La cantidad de espacio de datos dentro de un paquete también puede variar dentro de un medio determinado, en función de la disposición del encabezado del paquete. Por ejemplo, el tamaño de datos efectivo de un paquete Ethernet varía en función de si es del tipo Ethernet II, Ethernet 802,2 o Ethernet SNAP.

El *tamaño de paquete enrutable* refleja el tamaño de paquete máximo que un enrutador intermedio está dispuesto a reenviar. La mayoría de los enrutadores IPX se compilan para enrutar cualquier datagrama de tamaño siempre que permanezca dentro del tamaño del medio de la red de envío y recepción. Sin embargo, los enrutadores más antiguos pueden limitar el tamaño de paquete máximo a 576 bytes, incluidos los encabezados de protocolo.

El tamaño de paquete de la *estación final* refleja el tamaño de los búferes de escucha que las estaciones finales han publicado para recibir los paquetes entrantes. Incluso cuando los límites de medios y enrutadores permiten un paquete a través de, es posible que la estación final lo descarte si la aplicación receptora ha publicado un búfer más pequeño. Muchas aplicaciones IPX/SPX tradicionales limitan el tamaño del búfer de recepción, de modo que la parte de datos no debe tener más de 512 o 1024 bytes.

 

 



