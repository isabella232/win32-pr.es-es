---
description: El tamaño del paquete multimedia afecta a la capacidad de los protocolos IPX de transferir datos a través de redes y puede resultar difícil de tratar de forma independiente del transporte.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Acerca del tamaño del paquete multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03be30402dc94b22315292b281565572f04cbc89803eeed79f67d55a77ceeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412195"
---
# <a name="about-media-packet-size"></a>Acerca del tamaño del paquete multimedia

El tamaño del paquete multimedia afecta a la capacidad de los protocolos IPX de transferir datos a través de redes y puede resultar difícil de tratar de forma independiente del transporte. IPX no segmenta los paquetes, ni informa de cuándo se descartan los paquetes debido a infracciones de tamaño. Esto significa que alguna entidad de la estación final debe mantener el conocimiento del tamaño máximo de paquete que se usará en cualquier ruta de acceso de trabajo de Internet determinada. Tradicionalmente, los datagramas IPX y los servicios orientados a la conexión de SPX han dejado esta carga a la aplicación, mientras que SPXII ha usado grandes negociaciones de paquetes de Internet para controlarla de forma transparente.

Winsock intenta establecer límites de tamaño de paquetes razonables para sus distintos protocolos IPX, como se describe en la sección siguiente. Las aplicaciones pueden ver y modificar estos límites a través de las opciones de socket get/set. Al determinar el tamaño máximo de los paquetes, las tres áreas de preocupación son:

-   \# Tamaño del paquete multimedia
-   \# Tamaño de paquete enrutable
-   \# Tamaño de paquete de la estación final

*El tamaño del paquete multimedia* refleja el tamaño máximo de paquete aceptable en cualquier medio que el paquete atraviesa a su destino. El tamaño de los paquetes varía entre medios diferentes, como Ethernet y token ring. La cantidad de espacio de datos dentro de un paquete también puede variar dentro de un medio determinado, dependiendo de la disposición del encabezado del paquete. Por ejemplo, el tamaño de datos efectivo de un paquete Ethernet varía en función de si es del tipo Ethernet II, Ethernet 802.2 o Ethernet SNAP.

*El tamaño de paquete enrutable* refleja el tamaño máximo de paquete que un enrutador intermedio está dispuesto a reenviar. La mayoría de los enrutadores IPX se han creado para enrutar cualquier datagrama de tamaño, siempre y cuando permanezca dentro del tamaño del medio de la red de envío y recepción. Sin embargo, los enrutadores más antiguos pueden limitar el tamaño máximo del paquete a 576 bytes, incluidos los encabezados de protocolo.

*El tamaño del paquete de la estación* final refleja el tamaño de los búferes de escucha que las estaciones finales han publicado para recibir los paquetes entrantes. Incluso cuando los límites de medios y enrutadores permiten el paso de un paquete, la estación final puede descartarlo si la aplicación receptora ha publicado un búfer más pequeño. Muchas aplicaciones IPX/SPX tradicionales limitan el tamaño del búfer de recepción, de forma que la parte de los datos no debe tener más de 512 o 1024 bytes.

 

 



