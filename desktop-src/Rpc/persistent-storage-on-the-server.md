---
title: Almacenamiento persistente en el servidor
description: Puede optimizar la aplicación para que el código auxiliar del servidor no libere memoria en el servidor en el momento de la finalización de una llamada a procedimiento remoto.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994409"
---
# <a name="persistent-storage-on-the-server"></a>Almacenamiento persistente en el servidor

Puede optimizar la aplicación para que el código auxiliar del servidor no libere memoria en el servidor en el momento de la finalización de una llamada a procedimiento remoto. Por ejemplo, cuando un identificador de contexto se manipulará mediante varios procedimientos remotos, puede usar el atributo ACF **\[ allocate (no \_ disponible) \]** para conservar la memoria asignada en el servidor.

El atributo **\[ allocate (no \_ Free) \]** se agrega a la declaración de **definición** de tipo ACF en ACF. Por ejemplo:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Cuando se especifica el atributo **\[ allocate (no \_ Free) \]** , el código auxiliar de servidor asigna la estructura de datos de árbol, pero no la libera. Al hacer que los punteros a estas áreas de datos persistentes estén disponibles para otras rutinas, por ejemplo, copiando los punteros a variables globales, los datos retenidos son accesibles para otras funciones de servidor. El atributo **\[ allocate (no \_ gratuito) \]** es especialmente útil para mantener estructuras de puntero persistentes como parte de la información de estado del servidor asociada a un tipo de identificador de contexto.

 

 




