---
title: Uso de punteros opacos
description: A menudo, los clientes deben almacenar información adicional específica del cliente sobre los destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d24524f64fca7062ffb35ed6f4d5e6a2bc935ef7fee0c7fa141cb2e823e70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025075"
---
# <a name="using-opaque-pointers"></a>Uso de punteros opacos

A menudo, los clientes deben almacenar información adicional específica del cliente sobre los destinos. El administrador de tablas de enrutamiento permite a los clientes almacenar esta información en estructuras de destino en la tabla de enrutamiento. La información se almacena y recupera mediante *punteros opacos.* La información almacenada es privada y solo es accesible para el cliente que posee el puntero opaco.

Por ejemplo, el administrador de grupos de multidifusión mantiene una lista de entradas de reenvío de multidifusión que dependen de un destino determinado. El administrador de grupos de multidifusión usa un puntero opaco en ese destino. En otro ejemplo, un protocolo de enrutamiento que anuncia un destino determinado puede mantener información relacionada con su propio anuncio de ruta del destino mediante un puntero opaco, aunque no sea el propietario de la mejor ruta.

El número de punteros opacos es limitado; Estos punteros se asignan a los clientes por primera vez y por primera vez. El administrador del enrutador debe asignar el número correcto de punteros durante la configuración del enrutador; por lo tanto, los protocolos de enrutamiento y otros clientes deben documentar su uso de punteros opacos.

 

 




