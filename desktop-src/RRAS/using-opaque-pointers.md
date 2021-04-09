---
title: Usar punteros opacos
description: Los clientes a menudo deben almacenar información adicional específica del cliente acerca de los destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903668"
---
# <a name="using-opaque-pointers"></a>Usar punteros opacos

Los clientes a menudo deben almacenar información adicional específica del cliente acerca de los destinos. El administrador de tablas de enrutamiento permite a los clientes almacenar esta información en estructuras de destino de la tabla de enrutamiento. La información se almacena y se recupera mediante *punteros opacos*. La información almacenada es privada y solo es accesible para el cliente que posee el puntero opaco.

Por ejemplo, el administrador del grupo de multidifusión mantiene una lista de entradas de reenvío de multidifusión que dependen de un destino determinado. El administrador del grupo de multidifusión usa un puntero opaco en ese destino. En otro ejemplo, un protocolo de enrutamiento que anuncia un destino determinado puede mantener la información relacionada con su propio anuncio de ruta del destino mediante un puntero opaco, aunque no sea el propietario de la mejor ruta.

El número de punteros opacos es limitado; estos punteros se asignan a los clientes en función de la primera vez que se atiende. El administrador del enrutador debe asignar el número correcto de punteros durante la configuración del enrutador. por lo tanto, los protocolos de enrutamiento y otros clientes deben documentar el uso de punteros opacos.

 

 




