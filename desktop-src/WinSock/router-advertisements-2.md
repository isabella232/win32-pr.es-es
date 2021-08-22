---
description: El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento. Las rutas no publicadas se usan para el enrutamiento, pero se omiten al construir anuncios de enrutador.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Anuncios de enrutador IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef8a7be2139c03d94e8a84eae410e9f4f2e92da6059def1ef89997138009d351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612945"
---
# <a name="ipv6-router-advertisements"></a>Anuncios de enrutador IPv6

El contenido de los anuncios de enrutador IPv6 se deriva automáticamente de las rutas publicadas en la tabla de enrutamiento. Las rutas no publicadas se usan para el enrutamiento, pero se omiten al construir anuncios de enrutador.

Los anuncios de enrutador para IPv6 siempre contienen una opción de dirección de capa de vínculo de origen y una opción de MTU. El valor de la opción MTU se toma de la MTU del vínculo actual de la interfaz de envío. Este valor se puede cambiar con el comando ifc mtu de ipv6.

El anuncio de enrutador solo tiene una duración de enrutador distinta de cero si hay una ruta predeterminada publicada. Una ruta predeterminada es una ruta para el prefijo de longitud cero.

Las rutas publicadas en el vínculo tienen como resultado opciones de información de prefijo en los anuncios de enrutador. Si el prefijo en el vínculo tiene 64 bits, la opción de información de prefijo tiene los bits L y A establecidos y los hosts que lo reciben configurarán automáticamente las direcciones.

Una interfaz que envía anuncios de enrutador también configurará automáticamente las direcciones para sí misma en función de las opciones de información de prefijo que envía.

Se recomienda una duración finita de no duración en todas las rutas publicadas (por ejemplo, 30 minutos). Si decide retirar una ruta, puede cambiarla para que tenga una duración de vencimiento. La ruta se realizará a lo largo de varios anuncios de enrutador y desaparecerá tanto del enrutador como de cualquier host que reciba los anuncios del enrutador.

Las rutas que los hosts encuentran a través de la antigüedad de los anuncios de enrutador y no se publican. También se configura automáticamente a partir de la antigüedad de los anuncios de enrutador.

 

 



