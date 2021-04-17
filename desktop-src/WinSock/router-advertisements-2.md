---
description: El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento. Las rutas no publicadas se usan para el enrutamiento, pero se omiten cuando se crean anuncios de enrutador.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Anuncios de enrutador IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706186"
---
# <a name="ipv6-router-advertisements"></a>Anuncios de enrutador IPv6

El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento. Las rutas no publicadas se usan para el enrutamiento, pero se omiten cuando se crean anuncios de enrutador.

Los anuncios de enrutador para IPv6 siempre contienen una opción de dirección de nivel de vínculo de origen y una opción de MTU. El valor de la opción MTU se toma de la MTU de vínculo actual de la interfaz de envío. Este valor se puede cambiar con el comando IFC MTU de IPv6.

El anuncio de enrutador solo tiene una duración de enrutador distinto de cero si hay una ruta predeterminada publicada. Una ruta predeterminada es una ruta para el prefijo de longitud cero.

Las rutas en vínculo publicadas dan como resultado opciones de información de prefijo en anuncios de enrutador. Si el prefijo en vínculo tiene 64 bits, la opción de información de prefijo tiene el conjunto de bits L y un y los hosts que lo reciben configurarán las direcciones de forma autoconfigurada.

Una interfaz que envía anuncios de enrutador también configurará automáticamente las direcciones para sí misma basándose en las opciones de información de prefijo que envía.

Se recomienda una duración no caducante finita en todas las rutas publicadas (por ejemplo, 30 minutos). Si decide retirar una ruta, puede cambiar la ruta para que tenga una duración de caducidad. La ruta va a vencer en el transcurso de varios anuncios de enrutador y después desaparecerá del enrutador y de los hosts que reciban los anuncios de enrutador.

Las rutas que hospedan la búsqueda a través de anuncios de enrutador caducan y no se publican. Se trata también de la configuración de la antigüedad de los anuncios de enrutador.

 

 



